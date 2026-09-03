> there is no spoon. there is only the bug.

<p align="center">
  <img alt="what i actually do all day"
       src="https://readme-typing-svg.demolab.com/?font=JetBrains+Mono&weight=500&size=19&pause=1500&color=3FB950&center=true&vCenter=true&width=740&height=44&lines=i+point+a+camera+at+dead+electronics+and+a+servo+sorts+them;i+also+patch+open-source+banking+software;these+two+facts+are+unrelated+and+i+have+stopped+explaining+it;my+favourite+feature+is+the+one+that+refuses+to+answer" />
</p>

<p align="center">
  <img alt="merged upstream" src="https://img.shields.io/badge/merged%20upstream-7-3FB950?style=for-the-badge&labelColor=161b22" />
  <img alt="still open" src="https://img.shields.io/badge/still%20open-1-F5A524?style=for-the-badge&labelColor=161b22" />
  <img alt="load cells that lie" src="https://img.shields.io/badge/load%20cells%20that%20lie-1-DA3633?style=for-the-badge&labelColor=161b22" />
  <img alt="people who scrolled this far" src="https://komarev.com/ghpvc/?username=parth-sharma-10&label=people%20who%20scrolled%20this%20far&color=6e40c9&style=for-the-badge" />
</p>

```console
$ whoami
parth — b.tech computer engineering, learning by breaking real codebases

$ ps aux | grep -i obsession
  yolo11 pointed at a pile of e-waste ......... running
  mifos x, open-source core banking .......... running
  a trading signal i was fond of .............. killed by its own test suite

$ uptime
  shipping since 2025 · 7 merges upstream · no idea what i'm doing · continuing anyway
```

---

## stuff i built on purpose

<a href="https://github.com/parth-sharma-10/aurum">
  <img align="right" width="380"
       alt="aurum"
       src="https://socialify.git.ci/parth-sharma-10/aurum/image?description=0&font=Inter&forks=0&issues=0&language=1&name=1&owner=0&pattern=Circuit+Board&pulls=0&stargazers=0&theme=Auto" />
</a>

### aurum

started as *"can a webcam tell RAM apart from a CPU?"* — it now detects the
component, keeps an identity on it as it moves down a conveyor, weighs it, and
drives an arduino servo to put it in the right bin.

`YOLO11 · OpenCV · FastAPI · SQLite · Arduino · pytest`

271 files · 38 test files · green CI · weights shipped as a release asset
because github will not take my `.pt`

> favourite commit in the whole repo: **"refuse a railed converter instead of
> calling it 22 kg"**. the load cell had pinned to a rail and was reporting that
> as a measurement. it now says *i don't know*. that took longer to build than
> the part that says a number.

[`repo`](https://github.com/parth-sharma-10/aurum) · [`v0.1 weights`](https://github.com/parth-sharma-10/aurum/releases/tag/model-v0.1)

<br clear="right" />

### squall

i wanted to know whether a trading signal was real. it mostly wasn't — so it
became a research platform whose actual job is killing its own results.

`Python · LightGBM · PyTorch · Postgres · React · Docker`

leakage controls, walk-forward validation, block-bootstrap intervals,
multiple-testing correction. 298 files, 156 of them python, 69 of those tests.
one phase report grades itself `FRAGILE / NOT DEMONSTRATED / MARGINAL /
INCREMENTAL` and i left that in.

building something that reports a good number is easy. building something that
admits the number was one lucky draw is the part nobody writes tutorials about.

`private for now — ask me`

---

## stuff that happened anyway

at some point people started merging my patches into **Mifos X**, the
open-source core banking stack that sits on apache fineract. seven so far. i
still find this slightly funny.

**the one worth pointing at** —
[`mifos-reporting-plugin#537`](https://github.com/openMF/mifos-reporting-plugin/pull/537)
the reporting engine would execute whatever SQL a report design handed it. it
does not do that anymore. `+2,415 / −345`.

**the one that was funnier** —
[`web-app#3950`](https://github.com/openMF/web-app/pull/3950) deleted a github
pages deploy step that had failed on every push to `dev` since 9 july. net `−15`
lines. the branch build went green for the first time in eight weeks. best
outcome-per-line ratio i am ever getting.

the rest, briefly:

| | |
|---|---|
| [`web-app#3942`](https://github.com/openMF/web-app/pull/3942) | upload BIRT report designs from the UI |
| [`web-app#3858`](https://github.com/openMF/web-app/pull/3858) | notes stopped needing a manual refresh to appear |
| [`web-app#3509`](https://github.com/openMF/web-app/pull/3509) | made the error modal show the actual error |
| [`web-app#3058`](https://github.com/openMF/web-app/pull/3058) | stopped the UI offering to delete something it couldn't |
| [`web-app#3014`](https://github.com/openMF/web-app/pull/3014) | text that was too small, in a place people look a lot |

---

## currently open tabs

- getting BIRT report designs to upload per tenant —
  [`#543`](https://github.com/openMF/mifos-reporting-plugin/pull/543), still open
- calibrating that load cell properly, because one 180 g reference point is not
  a calibration, it's a wish
- a socratic DSA tutor that refuses to tell me the name of the pattern. i built
  it. it is deeply annoying. it works.
- a held-out bench eval set for aurum, so the numbers in my own README are ones
  i'd defend

---

## muscle memory

```text
python · typescript · java · sql
angular · react · fastapi · postgres
pytorch · ultralytics · opencv · lightgbm
arduino · pytest · playwright · docker · github actions
one (1) load cell that lies
```

---

## the contribution graph, being eaten

<picture>
  <source media="(prefers-color-scheme: dark)"
          srcset="https://raw.githubusercontent.com/parth-sharma-10/parth-sharma-10/output/snake-dark.svg" />
  <source media="(prefers-color-scheme: light)"
          srcset="https://raw.githubusercontent.com/parth-sharma-10/parth-sharma-10/output/snake.svg" />
  <img alt="a snake eating my commits"
       src="https://raw.githubusercontent.com/parth-sharma-10/parth-sharma-10/output/snake.svg" />
</picture>

<sub>generated nightly by an action in this repo, not by someone else's server —
half the widgets people paste into these things are returning 402 as i write
this.</sub>

<details>
<summary><b>things i have broken</b> &nbsp;<sub>(a partial list)</sub></summary>

<br />

- a load cell, which then insisted a DC converter weighed 22 kg
- a github pages deploy — already broken for eight weeks when i got there. i
  fixed it by deleting it.
- my own trading results. repeatedly. on purpose. that was the whole project.
- a serial port, by flooding it, at a demo, in front of people
- the CI. then the CI. then, memorably, the CI.

</details>

<details>
<summary><b>the numbers, if you insist</b> &nbsp;<sub>(they are not impressive yet)</sub></summary>

<br />

<img width="49%" alt="commit stats"
     src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=parth-sharma-10&theme=transparent" />
<img width="49%" alt="when i actually commit"
     src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=parth-sharma-10&theme=transparent&utcOffset=5.5" />

<img width="49%" alt="most committed language"
     src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=parth-sharma-10&theme=transparent" />
<img width="49%" alt="contribution streak"
     src="https://streak-stats.demolab.com/?user=parth-sharma-10&hide_border=true&background=00000000&stroke=8b949e&ring=3FB950&fire=DA3633&currStreakLabel=8b949e&sideLabels=8b949e&dates=8b949e&sideNums=8b949e&currStreakNum=3FB950" />

</details>

---

there's also a PHP app in here for booking EV chargers. it was a college
project. i'm leaving it up because pretending i started at pytorch would be a lie.

`¯\_(ツ)_/¯` &nbsp; [mail me](mailto:parthrsharma1002@gmail.com)
