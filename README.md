# Note on heroku, the web process will shutdown after idling, this cause the web and data source reload
* so if running on local machine, the source will not reload, it will not fetch the newest data even though refresh broswer
2020-05-10T10:31:10.177703+00:00 heroku[web.1]: Idling
2020-05-10T10:31:10.179814+00:00 heroku[web.1]: State changed from up to down
2020-05-10T10:31:11.048445+00:00 heroku[web.1]: Stopping all processes with SIGTERM
2020-05-10T10:31:11.084271+00:00 app[web.1]: [2020-05-10 10:31:11 +0000] [18] [INFO] Worker exiting (pid: 18)
2020-05-10T10:31:11.084322+00:00 app[web.1]: [2020-05-10 10:31:11 +0000] [10] [INFO] Worker exiting (pid: 10)
2020-05-10T10:31:11.084888+00:00 app[web.1]: [2020-05-10 10:31:11 +0000] [4] [INFO] Handling signal: term
2020-05-10T10:31:11.385620+00:00 app[web.1]: [2020-05-10 10:31:11 +0000] [4] [INFO] Shutting down: Master
2020-05-10T10:31:11.454991+00:00 heroku[web.1]: Process exited with status 0
* when open again in broswer
2020-05-10T10:58:43.432525+00:00 heroku[web.1]: Unidling
2020-05-10T10:58:43.456084+00:00 heroku[web.1]: State changed from down to starting
2020-05-10T10:58:49.873353+00:00 heroku[web.1]: Starting process with command `gunicorn covid19:server`
2020-05-10T10:58:52.076488+00:00 heroku[web.1]: State changed from starting to up
2020-05-10T10:58:51.892412+00:00 app[web.1]: [2020-05-10 10:58:51 +0000] [4] [INFO] Starting gunicorn 20.0.4
2020-05-10T10:58:51.892964+00:00 app[web.1]: [2020-05-10 10:58:51 +0000] [4] [INFO] Listening at: http://0.0.0.0:58560 (4)
2020-05-10T10:58:51.893091+00:00 app[web.1]: [2020-05-10 10:58:51 +0000] [4] [INFO] Using worker: sync
2020-05-10T10:58:51.897339+00:00 app[web.1]: [2020-05-10 10:58:51 +0000] [10] [INFO] Booting worker with pid: 10
2020-05-10T10:58:51.976966+00:00 app[web.1]: [2020-05-10 10:58:51 +0000] [18] [INFO] Booting worker with pid: 18
2020-05-10T10:58:56.678826+00:00 app[web.1]: /app/covid19.py:192: SettingWithCopyWarning:

# Covid19 Dashboard Web App using Python (Plotly Dash)
Create your own dashboard web app with free resources using python only
All tools stated here are free.

### Data source provided by Johns Hopkins University Center for Systems Science and Engineering (JHU CSSE):
https://systems.jhu.edu/

### Prerequisite:
* Basic python - numpy, pandas, matplotlib, [plotly dash](https://dash.plotly.com/)
* Basic knowledge of creating python virtual environment. Recommended using [pyenv](https://github.com/pyenv/pyenv) or [Anaconda](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)

### Tools:
* [VS Code](https://code.visualstudio.com/download), [Pycharm Community](https://www.jetbrains.com/pycharm/download) or your personal choice of IDE
* Python packages required as stated in `requirements.txt`
* Sign up [Heroku](https://www.heroku.com/) and [Mapbox](https://www.mapbox.com/)

## Version 1.0 Dashboard (Source Code - `covid19.py` included)
Comments are included in the source code `covid19.py` to assist you.  
**Click [here](https://covid19-dashboard-online.herokuapp.com/) to access the web app**  
![Ver 1.0 top](https://github.com/Unicorndy/covid19_dashboard/blob/master/image/1_git.png)
![Ver 1.0 bottom](https://github.com/Unicorndy/covid19_dashboard/blob/master/image/2_git.png)


* Just clone this git, deploy to your own free Heroku server, and you are ready to go. Guide to deployment from [Heroku official Guide](https://dash.plotly.com/deployment)
* Ensure all files and folders (except folder image) are deployed to Heroku server.
* Remember to create your personal [mapbox access token.](https://www.mapbox.com/) and edit in `covid19.py`
* Optional: Create your own [Addthis](https://www.addthis.com/) share button.
---
## Version 2.0 Dashboard based on bootstrap 4 (Source Code not included as it is still wip)
**Click [here](https://covid19dashboardsg.herokuapp.com//) to take a look at the web app**  
![Dark to Light Theme](https://github.com/Unicorndy/covid19_dashboard/blob/master/image/DarktoLightV2.gif)  
Time Map and Bar Chart animation created with [Flourish Studio](https://flourish.studio/) and easily embeded into Plotly Dash with html.Iframe.
![Time map and bar chart](https://github.com/Unicorndy/covid19_dashboard/blob/master/image/Mapandbarchartanimation.gif)
