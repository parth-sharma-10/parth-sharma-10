# hi, i'm parth

> there is no spoon. there is only the bug.

i point a camera at a pile of dead electronics and make a servo sort it.

the rest of my time goes into open-source banking software. these two facts are
unrelated and i've stopped trying to explain the overlap.

---

## stuff i built on purpose

### aurum

started as "can a webcam tell RAM apart from a CPU?"

it is now 271 files that detect components with YOLO11, keep an identity on each
physical object as it moves, weigh it on a load cell, work out roughly what it's
made of, and drive an arduino servo to put it in the right bin. 38 test files,
green CI, model weights shipped as a release asset because github does not want
my `.pt` file.

favourite commit in the whole thing: **"refuse a railed converter instead of
calling it 22 kg"**. the load cell had pinned to a rail and was reporting that
as a measurement. it now says *i don't know* instead. that took longer to build
than the part that says a number.

→ [parth-sharma-10/aurum](https://github.com/parth-sharma-10/aurum)

### squall

i wanted to know whether a trading signal was real. it mostly wasn't.

so it turned into a research platform whose actual job is killing its own
results — leakage controls, walk-forward validation, block-bootstrap confidence
intervals, multiple-testing correction. one phase report grades itself
`FRAGILE / NOT DEMONSTRATED / MARGINAL / INCREMENTAL` and i left that in.

156 python files, 64 of them tests. building something that reports a good
number is easy. building something that admits the number was one lucky draw is
the part nobody writes tutorials about.

→ private for the moment, ask me

---

## stuff that happened anyway

at some point people started merging my patches into **Mifos X** — the
open-source core banking stack built on apache fineract. seven so far. i still
find this slightly funny.

the one worth pointing at:
[`mifos-reporting-plugin#537`](https://github.com/openMF/mifos-reporting-plugin/pull/537)
— the reporting engine would execute whatever SQL a report design handed it. it
does not do that anymore. +2,415 / −345.

the one that was funnier:
[`web-app#3950`](https://github.com/openMF/web-app/pull/3950) deleted a github
pages deploy that had been failing the build for a week straight while everyone
assumed it was fine. net −15 lines. CI went green for the first time since
august. best outcome-per-line ratio i'm ever getting.

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

- getting BIRT report designs to upload per tenant
  ([#543](https://github.com/openMF/mifos-reporting-plugin/pull/543), still open)
- calibrating that load cell properly, because one 180 g reference point is not
  a calibration, it's a wish
- a socratic DSA tutor that refuses to tell me the name of the pattern. i built
  it. it is deeply annoying. it works.
- a held-out bench eval set for aurum, because the numbers in my own README
  should be ones i'd defend

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

there's also a PHP app in here for booking EV chargers. it was a college
project. i'm leaving it up because pretending i started at pytorch would be a
lie.

[email](mailto:parthrsharma1002@gmail.com)
