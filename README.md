# Event and RSVP Management

# Event Management and RSVP System

An integrated event management and RSVP system designed to connect Meetup.com, Discord, WordPress, and Google Calendar. This system aims to prevent Zoom bombing by vetting attendees via RSVP information and their interest in the event.

## System Overview

Our system connects various platforms:

1. **Meetup.com:** Source of initial event information.
2. **Discord & WordPress:** Platforms where users can RSVP to events.
3. **Google Calendar:** Centralized location for scheduling and tracking events.
4. **Zoom:** Platform used for hosting the events.


## Features

- **Event Synchronization:** The system pulls event data from Meetup.com and syncs it with Google Calendar. RSVP URLs will be generated for Discord and WordPress platforms.
- **RSVP Collection:** Users RSVP through Discord or the WordPress website, providing necessary information and stating their interest in the event.
- **RSVP Vetting:** To avoid Zoom bombers, the system checks the authenticity of the RSVP before providing the Zoom link.
- **Zoom Integration:** Zoom meeting links are securely distributed to vetted attendees.
- **Interest Tracking:** The system collects and tracks the interests of attendees for future event planning.
- **Attendee Feedback:** Post-event feedback collection for continuous improvement of the event hosting process.

## System Architecture

A high-level overview of the system architecture and how the different components interact.

```
+-------------+ +--------------+ +-----------------+ +-------------+
| Meetup.com | -->| Google |<-->| RSVP Collection |<-->| Discord & |
| (Event Src) | | Calendar | | & Vetting (Our | | WordPress |
+-------------+ | (Event Sync) | | System) | | (RSVP Src) |
+--------------+ +-----------------+ +-------------+
| ^
v |
+-------------+
| Zoom (Event |
| Hosting) |
+-------------+
```
## Installation & Setup

Step-by-step instructions on how to install and setup the system.
To install the project dependencies:

```shell
$ poetry install
```

Get Your API keys:

Meetup.com:

Visit the Meetup API page: https://www.meetup.com/api/
Follow their guide to register your app and obtain an API key.
Discord:

Visit the Discord Developer Portal: https://discord.com/developers/applications
Create a new application and navigate to the "Bot" section to get your token (API key).
WordPress:

WordPress does not provide an API key by default. You can, however, use a variety of plugins that provide API capabilities. JSON API User, for example, provides an API key that allows user registration and other functionalities: https://wordpress.org/plugins/json-api-user/
After installing and activating your chosen plugin, follow its specific instructions to obtain an API key.
Google Calendar:

Visit the Google Cloud Console: https://console.cloud.google.com/
Create a new project, enable the Google Calendar API for that project, and create credentials to get an API key.
Zoom:

Visit the Zoom App Marketplace: https://marketplace.zoom.us/
Click on the "Develop" dropdown in the top-right corner and select "Build App". Follow the prompts to create a JWT app, which will provide an API key and Secret.

Organize the using DOTENV:
.env

```
# .env

# Meetup API key
MEETUP_API_KEY=your_meetup_api_key_here

# Discord token
DISCORD_TOKEN=your_discord_token_here

# Wordpress API key
WORDPRESS_API_KEY=your_wordpress_api_key_here

# Google Calendar API key
GOOGLE_CALENDAR_API_KEY=your_google_calendar_api_key_here

# Zoom API keys
ZOOM_API_KEY=your_zoom_api_key_here
ZOOM_API_SECRET=your_zoom_api_secret_here

```

## Usage (TBD)

Guidelines on how to use the system, covering all features

To run the Streamlit application:

`$ streamlit run app.py`


## Contributing (TBD)

Details for developers or interested parties on how to contribute to the project.

## License (TBD)

Information about the project's license.

## Contact Information (TBD)

Details on how to get in touch with the project team or maintainers.
