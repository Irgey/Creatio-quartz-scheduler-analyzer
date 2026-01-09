# Scheduler.log Analyzer

Lightweight web-based tool for analyzing **Creatio Scheduler.log** files.  
No backend, no installation, no build step.

---

## Purpose

The tool provides:
- JobStart statistics grouped by job class
- Date/time filtering
- Total and filtered JobStart counts
- Time-based JobStart load visualization
- Scheduler configuration inspection (`LogSchedulerConfiguration`)

---

## Input

- `Scheduler.log` from on-site Creatio (**Net.Framework 0/Log/Scheduler.log**)
- Plain text, standard scheduler log format
- Large files supported (stream parsing)

---

## Usage

1. Open `index.html` in a browser
2. Click **Choose Scheduler.log file**
3. (Optional) Set **From / To** and click **Apply**
4. Click **Visualise jobs** to render the chart

Date/time format:
```
YYYY-MM-DD HH:mm:ss,SSS
```

---

## Chart

- Stacked bar chart (Chart.js)
- Automatic time bucketing
- Top-N job classes + **Other**
- Tooltip shows per-class breakdown and total JobStart per bucket

Timestamps are interpreted exactly as written in the log (no timezone assumptions).

---

## Files

```
/
├── index.html
├── chart.umd.min.js
└── README.md
```

---

## Technical Notes

- Fully offline
- No external services
- Runs entirely in the browser

---

## Intended Use

- Scheduler load analysis
- Peak detection
- Troubleshooting and support
