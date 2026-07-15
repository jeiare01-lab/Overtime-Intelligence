# Overtime Intelligence Dashboard v2
## PGB Construction & Manufacturing | Enterprise Staffing Analysis Tool

---

## What Is This?

A **browser-based strategic tool** that analyzes overtime data and answers the question:

> **"How many people do we need to hire to fix our burnout problem?"**

Instead of just showing metrics, the dashboard calculates:
- **Workback:** "To reach 5% OT, hire X FTEs at cost $Y"
- **Workforward:** "If we do nothing for 3 months, cost will be $Z"
- **Risk Register:** "These specific people are quitting—here's who and when"
- **Hiring ROI:** "Paying $150K to hire 2 people saves $430K in OT + turnover"

**Audience:** CHRO, SBU MDs, HR Strategic Partners, Finance

---

## How to Use

### 1. **Get Your Data**
Export from PGB HR System (or Payroll):
- Cut-off period (e.g., June 2–17)
- Columns: Department, Cost Center, Employee, Regular Hours, Overtime Hours, Overtime %
- Format: CSV

**Example:**
```
Department,Cost Center,Employee,Regular Hours,Overtime Hours,Overtime %
P&L,PLD,CAHAPONON JOEBERT A,98.25,112.25,114.25%
P&L,PLD,JABINES JR.,95.84,76.33,79.65%
```

### 2. **Upload to Dashboard**
1. Go to: `https://yourusername.github.io/overtime-intelligence-dashboard/`
2. Drag/drop your CSV file
3. Dashboard auto-detects format
4. Click "Generate Analysis"

### 3. **Adjust Parameters (Optional)**
- **Target OT %:** What's your goal? (Default: 5%)
- **Hourly Loaded Cost:** Your blended rate. (Default: $35/hr)
- **Months Forward:** How far to project? (Default: 3 months)

### 4. **Read the Analysis**

#### **Executive Summary**
- **Status:** 🚨 CRISIS / ⚠ ELEVATED / ✓ WATCH
- **What it means:** Plain language on what the data says
- **Business impact:** Turnover risk, quality risk, cost
- **Decision required:** "CHRO to SBU MD: Approve hiring or expect resignations"

#### **Key Findings**
- Top 3 departments in crisis
- Extreme outliers (people working 100%+ OT)
- Root cause hypothesis

#### **Workback Card** (Hiring Scenario)
**If you want to reduce OT from 12% to 5%:**
- FTEs Needed: `2`
- Hiring Cost: `$150,000`
- Current OT Cost: `$130,000/month`
- OT Cost at 5%: `$50,000/month`
- Monthly Savings: `$80,000`
- **Payback Period: 1.9 months** ← Hiring pays for itself

#### **Workforward Card** (Cost of Inaction)
**If you do nothing for 3 months:**
- OT Cost: `$180,000`
- Expected Resignations: `4–5 people`
- Turnover Cost: `$450,000+` (recruiting + ramp + lost productivity)
- **Total Cost of Inaction: $630,000+**

**The Math:**
- Hire 2 FTEs: `$150K cost` → saves `$430K` → net gain of `$280K`
- Do nothing: `$630K cost` + brand damage + customer risk

#### **Risk Tiers**
- **🚨 CRITICAL (>50% OT):** Already mentally left. Working 100+ hrs/week. Resign within 30 days unless relief given.
- **⚠ HIGH (25–50% OT):** Sustainable 2–3 weeks. Monitor closely.
- **⚠ MEDIUM (10–25% OT):** Project surge range. Acceptable if phased.
- **✓ LOW (<10% OT):** Healthy. Keep as baseline.

#### **Charts**
- **Dept Chart:** Average OT by department (color-coded by severity)
- **Employee Chart:** Top 15 people with highest OT (the extreme cases)

### 5. **Export & Share**

**Three exports:**

1. **Executive Summary**
   - One-pager for CHRO/SBU MD
   - Status + findings + hiring recommendation
   - Good for board prep or investor calls

2. **Risk Register (CSV)**
   - List: Employee | Department | OT% | Risk Tier | Action
   - Send to managers: "Here are your high-risk people—check in this week"
   - Track which people rotate off projects vs. leave

3. **Workback Analysis (CSV)**
   - For Finance discussion: "Here's the hiring scenario we're proposing"
   - Shows cost/benefit/payback math in format finance understands

---

## What the Data Means

### **OT % Interpretation**

| OT % | What It Means | Hours/Week | Status |
|------|---------------|-----------|--------|
| <5% | Healthy. Normal workload. | +2 hrs/week | ✓ OK |
| 5–10% | Acceptable surge. Project work. | +2–4 hrs/week | ✓ OK |
| 10–25% | Project phase. Sustainable 4–6 weeks. | +4–10 hrs/week | ⚠ Watch |
| 25–50% | Elevated. Burnout risk if >3 weeks. | +10–20 hrs/week | 🔴 Act |
| 50–100% | Critical. Already checking job boards. | +20–40 hrs/week | 🚨 Crisis |
| >100% | RESIGN IMMINENT. Working 80+ hrs/week. | 40+ hrs/week | 🚨 LEAVE SOON |

### **Real Example: TOLO, VHIC ANDREW C @ 165% OT**
- Regular hours: 97.51
- Overtime: 160.94
- **Total work week: 258.45 ÷ 5 = ~51.7 hours/day**
- **Meaning:** Working 6 hours, then going home and working another 6 hours
- **Reality:** Already left emotionally. Resignation expected within 2 weeks.

### **Department Example: P&L @ 82.75% OT**
- Everyone in P&L is working ~33 extra hours per 40-hour week
- This is not sustainable for even 2 weeks
- Root cause: Staffing gap (hire), workload spike (rotate), or process issue (fix)

---

## When to Use This Tool

### **Weekly Standup** (CHRO + HR Core Team)
- Upload latest OT data
- "Our CRITICAL count went from 3 to 5. That's 2 new cases. Escalate hiring approval to SBU MD today."
- Export Risk Register → send to managers

### **Monthly SBU HR Heads Sync**
- "Construction avg OT down to 8% from 12%—hiring is working"
- "Maritime now at 14% OT—on target, continue current pace"
- "Real Estate spiked to 18%—new project? Or staffing issue? Let's investigate together"

### **Quarterly Board Prep**
- "People strategy is working: Despite 20% revenue growth, OT is flat—productivity gains"
- OR: "We invested $400K in 5 new hires—recovered $250K in OT cost + prevented $1.5M in turnover"

### **SBU MD Conversation** (Urgent)
- **Before:** "We have an overtime problem"
- **After:** "We have 4 people at critical OT (>100%). Without hiring relief, expect 2–3 resignations in 4 weeks. If we hire 2 FTEs now, we break even in 1.8 months and hit 5% OT target."
- Show workback card. Close deal.

### **Succession/Retention Planning**
- Risk Register shows who's about to leave
- Prioritize retention conversations with CRITICAL tier
- Plan backfill hiring proactively (not reactively post-resignation)

---

## How It Works (Technical)

- **Client-side only:** All processing happens in your browser. No data sent to servers.
- **Data privacy:** Upload CSV → Dashboard analyzes → You export summaries. Nothing persists.
- **No login needed:** Works on any device (desktop, tablet, phone).
- **Offline capable:** After first load, works without internet (modern browser only).

---

## Sample Data Format

Your CSV must have these columns (exact names):

```
Department,Cost Center,Employee,Regular Hours,Overtime Hours,Overtime %
```

**Real example from PGB:**
```
P&L,PLD,CAHAPONON JOEBERT A,98.25,112.25,114.25
P&L,PLD,JABINES JR. APOLINAER C,95.84,76.33,79.65
OM,OM-LH,VILLARINO ALMARIO F,95.01,20.07,21.12
```

**Column definitions:**
- **Department:** Functional group (P&L, OM, HRD, ITD, etc.)
- **Cost Center:** Sub-department (PLD, OM-LH, etc.)
- **Employee:** Full name as in payroll
- **Regular Hours:** Hours worked at normal rate (this period)
- **Overtime Hours:** Hours worked at OT rate (this period)
- **Overtime %:** OT Hours ÷ Regular Hours × 100

---

## FAQs

**Q: Does my data get saved?**  
A: No. Everything runs in your browser. Close the tab and it's gone. Export summaries if you want to keep them.

**Q: Can multiple people use it at the same time?**  
A: Yes. Each person uploads their own data, gets their own analysis. No conflicts.

**Q: What if my CSV has different column names?**  
A: Dashboard tries to auto-detect. If it fails, rename your columns to match exactly (case-sensitive).

**Q: How often should I upload data?**  
A: Weekly (if you have weekly OT reports) or bi-weekly/monthly. Frequency depends on your payroll cycle.

**Q: What if the hiring math seems wrong?**  
A: Adjust hourly rate. Default is $35/hr loaded cost. PGB might be higher. Try $45–50/hr for leadership roles.

**Q: Can I share this with external partners?**  
A: Yes. Dashboard is public. Just don't upload confidential employee data if sharing with consultants—export summaries instead.

**Q: What if OT is trending down—should I still hire?**  
A: Depends. If down because of recent hires, hiring worked. If down because of project completion, staffing was project-based and you're fine. Workforward helps you decide.

---

## Outputs Explained

### **Executive Summary** (Text Export)
**For:** CHRO, Board, SBU MDs  
**Use:** Pre-read before meetings. Answers "what's happening and why"  
**Length:** 1–2 pages

### **Risk Register (CSV)**
**For:** HR Strategic Partners, Department Managers  
**Use:** "Here are your people at risk—action plan needed"  
**Columns:** Employee | Department | OT% | Risk Tier | Action  
**Action:** Import into spreadsheet, track manager conversations, monitor who rotates/leaves

### **Workback Analysis (CSV)**
**For:** Finance, SBU MD  
**Use:** Hiring scenario justification. "If we hire 2 people at $150K, we save $430K in 6 months"  
**Columns:** Metric | Value  
**Format:** Simple key-value for finance pivot tables

---

## Support & Feedback

**Dashboard not working?**
- Try different browser (Chrome, Firefox, Safari)
- Refresh page (Ctrl+Shift+R or Cmd+Shift+R)
- Check CSV format (see sample data above)

**Want to add features?**
- Real-time email alerts when critical cases hit threshold
- SBU comparison charts (Construction vs. Real Estate vs. Maritime)
- Trend projections (will OT get worse or better?)
- Integration with PGB HR System for auto-refresh
- Tell us!

**Share feedback:**
- Paulette D. Liu (CHRO)
- James Villalon (GHR)
- Your HR Strategic Partner

---

## Versions

**v1:** Basic metrics + risk tiering  
**v2 (Current):** + Workback/Workforward hiring analysis + Auto-generated findings + Department/employee charts  
**v3 (Roadmap):** + Real-time alerts, SBU benchmarking, trend ML

---

**Dashboard Live At:**  
`https://[your-github-username].github.io/overtime-intelligence-dashboard/`

**Last Updated:** July 2026  
**Maintained By:** PGB HR Innovation Lab
