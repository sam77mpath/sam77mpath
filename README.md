name: Generate Profile Metrics

on:
  schedule:
    # Runs every 6 hours
    - cron: "0 */6 * * *"
  workflow_dispatch: {}
  push:
    branches:
      - main

permissions:
  contents: write

jobs:
  metrics:
    runs-on: ubuntu-latest
    steps:
      - name: Generate metrics.svg
        uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
          user: ${{ github.repository_owner }}
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Asia/Kolkata

          # Plugins
          plugin_languages: yes
          plugin_languages_analysis_timeout: 15
          plugin_languages_categories: markup, programming
          plugin_languages_limit: 8

          plugin_habits: yes
          plugin_habits_facts: yes
          plugin_habits_charts: yes

          plugin_achievements: yes
          plugin_achievements_display: compact

          plugin_topics: yes
          plugin_topics_limit: 10

          plugin_stars: yes
          plugin_stars_limit: 4

          plugin_lines: yes

          output_action: commit
          output_action_committer_name: metrics-bot
          output_action_committer_email: metrics-bot@users.noreply.github.com
          output_action_commit_message: "chore(metrics): update profile metrics [skip ci]"
