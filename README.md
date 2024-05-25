Plausible analytics data into Home Assistant

**Requirements:**
- Home Assistant
- Plausible (self hosted)

**Info:**
I'm not affiliated to Plausible in anyway! I'm sharing this to give something back to the community.
I'm not an expert in HA or Plausible so if you want to improve or add something, I'd love to hear from you!

In short what this software is and does:
An alternative to Google Analytics but works without cookies and it's opensource. See their website here: https://plausible.io
I'm using it in a docker image (fully self hosted).
It could work differently if you use Plausible cloud, so to know if it works the same way, you can find out for yourself.

**Features:**
- Retrieve the amount of (unique) visitors, pageviews, bounce rate, visit duration etc. from your website(s).
- Perform api checks to see whether the Plausible api/app, clickhouse and database (postgres) are running as expected.

**Steps to do:**
1. Open Plausible, settings and create a new API key.
2. Create a new HA input_text helper and store the API key there.
3. Change the resource (2x) to your own IP address where you host Plausible.
4. Change siteid to your own website domain name.
5. It's now set to 'period=day' but you can change it to something else if you want: see the available options [here](https://plausible.io/docs/stats-api#time-periods).

Have fun!

More info about the API: https://plausible.io/docs/stats-api
