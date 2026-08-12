## Hi there 👋

name: metrics
on:
  schedule: [{cron: "0 0 * * *"}]
  workflow_dispatch:
jobs:
  metrics:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          filename: metrics.svg
          token: ${{ secrets.METRICS_TOKEN }}
          plugin_languages: yes
          plugin_habits: yes
          plugin_stars: yes!--
