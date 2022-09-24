## STAR
[![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=DenverCoder1)](https://git.io/streak-stats)

## Winner
[![trophy](https://github-profile-trophy.vercel.app/?username=ryo-ma)](https://github.com/ryo-ma/github-profile-trophy)

## Card
[![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=anuraghazra&repo=github-readme-stats)](https://github.com/anuraghazra/github-readme-stats)


## Snake Eating my contribution
![snake gif](https://github.com/salak96/salak96/blob/output/github-contribution-grid-snake.gif)


## Sosial_Media
<h3 align="left">Connect with me:</h3>
<p align="left">
<a href="your link" target="blank"><img align="center" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/twitter.svg" alt="" height="30" width="40" /></a>
<a href="your link" target="blank"><img align="center" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/linkedin.svg" alt="" height="30" width="40" /></a>
<a href="your link" target="blank"><img align="center" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/instagram.svg" alt="" height="30" width="40" /></a>
<a href="your link" target="blank"><img align="center" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/youtube.svg" alt="" height="30" width="40" /></a>
</p>

## Theme
name: Latest blog post workflow
on:
  schedule: # Run workflow automatically
    - cron: '0 * * * *' # Runs every hour, on the hour
  workflow_dispatch: # Run workflow manually (without waiting for the cron to be called), through the GitHub Actions Workflow page directly

jobs:
  update-readme-with-blog:
    name: Update this repo's README with latest blog posts
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: Pull in dev.to posts
        uses: gautamkrishnar/blog-post-workflow@v1
        with:
          feed_list: "https://dev.to/feed/gautamkrishnar,https://www.gautamkrishnar.com/feed/"
