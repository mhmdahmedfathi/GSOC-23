# Project Name

GSOC'23 user managment

### Part 1: Authentication

As part of my contributions to the project, I fixed the code related to user authentication. Specifically, I worked on the login, signup, forget password, reset password, and personal page features. This involved identifying and fixing bugs in the existing code, as well as implementing new functionality where necessary.

### Part 2: Notification Flow

In addition to the authentication work, I also implemented a notification flow feature. This allows users to choose which notification channels they want to receive updates on (e.g. email, Slack, Discord), and then receive notifications when any of their selected networks has any deviation.

If a user chooses Discord as their notification channel, they will be prompted to enter information about which channel they want to receive notifications in. Once this information is provided, the user will be redirected to a Discord page where they will be given a code. This code is then sent to the backend, which uses it to make a request to the Discord API and retrieve information about the user and access token. This information is then saved for future use.

The same applies to the slack api, If a user chooses Slack as their notification channel, they will be prompted to enter information about which channel they want to receive notifications in. Once this information is provided, the user will be redirected to a Discord page where they will be given a code. This code is then sent to the backend, which uses it to make a request to the Slack API and retrieve information about the user and access token. This information is then saved for future use.

This is a project that includes a background worker using Celery and a scheduler using Celery beat. The worker runs once every hour and is connected to Kafka. It checks for any unread alarms for the tasks group and if there are any, it gets all the users that listen to this network. It then checks if the user has a notification flow using any of the channels (email, Discord, Slack) and if yes, it sends an alarm message using that channel to notify the user.

#### Screenshots

![Screenshot from 2023-07-26 21-31-02](https://github.com/mhmdahmedfathi/GSOC-23/assets/52926511/ca33556a-f1c8-420d-88e5-c01bbc4c5d34)
![Screenshot from 2023-07-26 21-31-23](https://github.com/mhmdahmedfathi/GSOC-23/assets/52926511/28987db4-1a65-4b24-ac46-cab7fc2e680e)
![Screenshot from 2023-07-26 21-45-35](https://github.com/mhmdahmedfathi/GSOC-23/assets/52926511/a1139c7d-8a90-4fe3-b1cb-ed62b037c971)
![Screenshot from 2023-07-26 21-45-48](https://github.com/mhmdahmedfathi/GSOC-23/assets/52926511/108250ff-3d18-41c6-8e64-c0c937d8fd16)
![Screenshot from 2023-07-26 21-45-56](https://github.com/mhmdahmedfathi/GSOC-23/assets/52926511/bceeceec-9d6c-4860-8367-43eecebca984)
![Screenshot from 2023-07-26 21-46-24](https://github.com/mhmdahmedfathi/GSOC-23/assets/52926511/f397a255-4014-4ab8-b4c0-6d3ced31c21a)
![Screenshot from 2023-09-17 23-33-29](https://github.com/mhmdahmedfathi/GSOC-23/assets/52926511/ed55d89b-46c3-4d54-8c17-701184a88d1d)
![Screenshot from 2023-09-17 23-34-28](https://github.com/mhmdahmedfathi/GSOC-23/assets/52926511/d2eb7757-0d01-4e00-9d9e-7682dd183d96)
![Screenshot from 2023-09-17 23-34-36](https://github.com/mhmdahmedfathi/GSOC-23/assets/52926511/87f60b19-a060-47aa-a31c-3afb729182cb)
![Screenshot from 2023-09-17 23-35-06](https://github.com/mhmdahmedfathi/GSOC-23/assets/52926511/d88aabe4-a300-4ffb-a5b8-28c8955adbe4)
![Screenshot from 2023-09-17 23-35-14](https://github.com/mhmdahmedfathi/GSOC-23/assets/52926511/026592e9-3343-4fc2-8848-d40f239148ed)
![Screenshot from 2023-09-17 23-35-43](https://github.com/mhmdahmedfathi/GSOC-23/assets/52926511/5999f6b5-73fe-4917-bd8c-8991e7ad62a1)
![Screenshot from 2023-09-17 20-24-37](https://github.com/mhmdahmedfathi/GSOC-23/assets/52926511/7de08fc5-9709-455d-9ab2-be8ad43fed5a)


## Conclusion

Overall, my contributions to this project involved fixing authentication-related bugs and implementing a new notification flow feature. I believe that these changes will improve the user experience and make the project more useful for its intended audience.
