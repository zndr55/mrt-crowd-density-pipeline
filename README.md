# MRT Crowd Density Pipeline

An Alteryx workflow from my Distributed Data Pipelines module (Apr 2026 semester). The question I wanted to answer: are Circle Line interchange stations more crowded than the other stations on the line?

It pulls from three LTA DataMall APIs:

- Station Crowd Density Real Time
- Station Crowd Density Forecast (evening peak, 30-minute steps)
- Train Service Alerts

The train line code is a single input at the start of the workflow (CCL by default), so it can be pointed at another line. Stations are tagged as interchange or non-interchange, summarised by crowd level, and put into one HTML dashboard. The Analytic App version adds a drop-down so you can look at one station at a time.

On my run (Sat 1 Aug 2026), 2 of the 9 interchange stations were at moderate crowding against 0 of the 25 other stations. That is one snapshot, so it only points in the direction of the idea. The only "high" reading was Stadium, which I put down to events at the Sports Hub.

## Files

- `Final_Dashboard.htm`: the dashboard output from my run
- `workflow/mrt_crowd_density_app.yxwz`: the Alteryx Analytic App

## Running it

You need Alteryx Designer and your own free AccountKey from LTA DataMall. I removed my key from the workflow, so open the three Download tools and put yours in the `AccountKey` header (Headers tab) in place of `YOUR_API_KEY`.
