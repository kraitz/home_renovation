# Home Renovation Decision Support Dashboard

An interactive Tableau dashboard that helps prioritize home renovation projects against a fixed annual budget. Built on a simulated project-planning dataset — values are fictional but informed by realistic regional renovation costs and ROI estimates.

**[View the live dashboard on Tableau Public →](https://public.tableau.com/app/profile/kraitz/viz/home_renovation_decision_support_tool/Dashboard1ExecutiveOverview)**

## The problem

We have more renovation ideas than budget or time to execute them. Some projects add resale value, some just make daily life better, and some can be partly DIY'd to free up cash for other work. Before committing a year of budget to a project list, I wanted a single view that could answer:

- How much have we spent, and how much is left in this year's budget?
- Are we currently over or under budget, and by how much?
- Which rooms or areas of the house are driving the majority of our costs?
- Within the highest-cost area, which specific projects are responsible?
- Is a given project worth doing based on cost vs. the value it adds — and how much daily use / ROI does it deliver relative to that cost?

## How it works

**1. KPI summary tiles (top of dashboard)**
Top-level KPIs provide an at-a-glance check of completion progress, total estimated cost, potential DIY savings, remaining budget, and projected home value increase.

**2. Cost vs. Annual Budget**
This chart compares actual/estimated spend against the budget set for the selected year. Hovering shows a tooltip calling out whether you're over or under budget and by how much, plus the potential DIY savings available (ie the amount you could claw back by tackling a project yourself instead of hiring it out). That DIY figure is meant to double as a lever: if you're over budget, this is where you'd look for room to offset it.

**3. Areas of the home (cost breakdown)**
A chart breaking down cost by room/area for the selected year, so you can see at a glance which part of the house is eating the largest share of the budget. Clicking a room in the areas chart filters the detail table/scatterplot down to just the projects in that room — so you go from "the kitchen is our biggest cost center this year" to "here's exactly which three kitchen projects are responsible."

**4. Cost vs. Value Increase scatterplot**
The drill-down view plots individual projects on cost vs. estimated home value increase, effectively splitting projects into quadrants (e.g., low-cost/high-value being the easy wins). Point size and color encode ROI and daily use score, so you can spot a project that's not just financially efficient but also gets used constantly — versus one that pencils out on paper but you'd rarely touch.

**5. Year filter**
A dropdown parameter located at the top of the dashboard next to the title lets you switch the entire dashboard between "All Years" and a specific planning year. Every chart recalculates against just that year's projects, so you can plan year-by-year instead of looking at the whole multi-year plan at once.

## Future improvements

- **Redesign the completion progress bar** — replace the current bar with a rounded/pill-style progress indicator for a cleaner look.
- **"Move project" what-if simulator** — let a user select a project and reassign it to a different planning year via a parameter, with the budget and cost charts recalculating against that simulated year. This would turn the dashboard from a reporting tool into an actual planning tool: "what happens to next year's budget if we push the deck rebuild out to the year after?"
- **Additional dashboard views** — Prioritization view (given a fixed budget, what should be tackled first) to complement the current Investment/ROI-focused Executive Overview.
- **Dependencies flow chart** — Some projects cannot be started until after different projects are completed. I'd like to create a flow chart and identify the projects that are creating the biggest bottlenecks in the renovations process, perhaps comparing the bottlenecks against cost or ROI to understand better how viably we can fit the bottleneck project into the annual budget.

## Repo contents

- `dashboard.twbx` — packaged Tableau workbook (data included)
- `images/` — static screenshots for anyone browsing without Tableau
