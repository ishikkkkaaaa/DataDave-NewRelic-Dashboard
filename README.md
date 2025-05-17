![New Relic logo](https://newrelic.com/static-assets/images/logo/nr-logo-50vh.png)
# Introduction
If you don't already know why you need a monitoring and observability solution, it can be challenging to find an example that is illustrative, compelling, and engaging. There are literally thousands of "monitor this fake take-out food website" examples and - while they certainly show a valid real-world example of something you might want to monitor - they are usually a real yawner.

What if - and hear us out - you could play around with a monitoring solution AND PLAY A VIDEO GAME at the same time?!? WE KNOW, RIGHT?!?

That's what this example is all about. Install a game, set it up in New Relic, and then play the game to see your stats.

Dangerous Dave was a classic 1980's side-scroller style game that many spent hours playing when we should have been doing productive work. Now we've turned the tables, making Dave help with our actual work.

The point of this project is two-fold:

 1. To give folks a fun way to kick the tires on New Relic monitoring;
 2. and to show how easy it is to instrument a custom application, capture and collect non-standard metrics, and display them in a meaningful way.

We hope you enjoy!

---

## Assignment

This assignment involves setting up monitoring for your game using New Relic's Python Agent. Your goal is to collect data (telemetry) about how players interact with the game.

**What you need to do:**

*Instrument the game code*: You'll need to add code snippets to your game's Python code (game.py) to capture specific data points. These code snippets will utilize APIs provided by the New Relic Python Agent SDK.

*Capture custom telemetry*: Focus on capturing data that's unique to your game and provides valuable insights.

You can capture the custom telemetry from the game that will require specific APIs from the New Relic Python Agent SDK.

### Sample Instrumentation


You will find one <u>function already instrumented</u> and one instance of <u>custom instrumentation</u> on line:277 in `game.py`

```python
# Record custom New Relic event [RLF]
event_type = "GameIncomplete"
params = {'current_level': current_level_number, 'player_score': GamePlayer.score}
newrelic.agent.record_custom_event(event_type, params, application=application)
```

**HINT**: The placeholders are included to help you setup the instrumentation. Look for the following comment in the `game.py`

```python
# Record custom New Relic event [RLF]
```

---

## Prerequisites

- You'll need a New Relic account. The good news is that you can create a [free account here](https://newrelic.com/signup?utm_source=event&utm_medium=community&utm_campaign=apj-fy-24-q1-devrel-kcdmumbai) (no credit card required).
- To run the program, you must have Python 3 installed.
- You will need to install the following packages using `pip` before starting the program. You may wish to install these packages in a [virtual environment](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/).
  - pygame (e.g. `pip3 install pygame`)

---


## Primary Goals and Expected Outcomes:

1. New Relic instrumentation

- Set up instrumentation for the application.

- Update the newrelic.ini file by replacing INSERT_YOUR_INGEST_LICENSE_KEY_HERE with your account's [ingest license key](https://docs.newrelic.com/docs/apis/intro-apis/new-relic-api-keys/).

2. Setup Custom Dashboard

  - To see your game stats on a New Relic dashboard edit the [game_stats.json](game_stats.json) file by doing a global search and replace to substitute "YOUR_ACCOUNT_ID" with your 7-digit [account ID](https://docs.newrelic.com/docs/accounts/accounts-billing/account-structure/account-id/).

  - Then, copy the modified JSON and [import the dashboard](https://docs.newrelic.com/docs/query-your-data/explore-query-data/dashboards/introduction-dashboards/#dashboards-import) into your New Relic account.
<br>
3. Custom Instrumentation
  - Evaluate the [game_stats.json](game_stats.json) and setup custom instrumentation for all the custom events similar to the example provided in the `game.py`.
  - Capture **MOST** of the events if not all. You can find the details of the custom events in the provided dashboards file. 
  - Refer to the sample of the [populated dashboard](Game_Stats-Dashboard_sample.pdf) (file:Game_Stats-Dashboard_sample.pdf) included in the zip folder
<br>
4. Documentation (Optional)
  - Document the changes you made to the codebase and the steps you took to set up the New Relic account and dashboard.
  - Include any challenges you faced and how you overcame them.

---

## Submission:
Submit the Assignment with instrumented codebase in a Git repository along with your New Relic Account ID and email address used for creating the New Relic Account.

---

## Running the program

- You can run the game by running the main python script located at the root of the repository: `python3 game.py`. This should start the game immediately.

---

## Troubleshooting

- If the game is crashing or you are unable to run the game, make sure you have complete the prerequisites above especially the ENV VAR and adding New Relic License Key to the `newrelic.ini` file.
- After adding the ENV VAR (`export NEW_RELIC_CONFIG_FILE=/Users/username/Downloads/dangerous-dave/newrelic.ini`), launch the game using the binary from the same terminal instance. Alternatively you can add the ENV VAR to your `.bashrc`, `.zshrc` or `.bash_profile` file and restart your terminal session.


---


### Dangerous Dave Replica
*(this is the original description you can find over on https://github.com/mwolfart/dangerous-dave) We remain deeply indebted to them for their effort to bring this classic game to life on the python platform! - Rachel and Leon)*

 - This project is a replica of the 1988 DOS game Dangerous Dave, made by John Romero. The project was built in Python along with a team of three students (Arthur Medeiros, Guilherme Cattani and me), as a course assignment.
 - The goal of the project was to study and practice the three types of programming paradigms: imperative, object-oriented and functional. To achieve this, we picked Python as a language since it can perform all three types of tasks in a fairly good way.
