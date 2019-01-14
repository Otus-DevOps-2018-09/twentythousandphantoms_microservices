# twentythousandphantoms_microservices

### Travis & Slack Integration (Notifications)

1. Slack & GitHub Integration: https://get.slack.help/hc/en-us/articles/232289568-GitHub-for-Slack
  
   Go to <your_project>.slack.com → Type into your Slack channel (e.g. "#andrey_belov"):   

   ```
   /github subscribe Otus-DevOps-2018-09/twentythousandphantoms_microservices commits:all
   ```

2. Slack & Travis Integration: https://docs.travis-ci.com/user/notifications/

   Go to <your_project>.slack.com → Add Apps... → Travis CI → Settings → Add Configuration → Choose Channel (e.g. "#andrey_belov") → Add Travis Integration → Remember the token. Then run commands:

   ```
   $ gem install travis
   $ travis login --org
   $ travis encrypt "devops-team-otus:<private_token>#andrey_belov" --add notifications.slack.rooms --org 
