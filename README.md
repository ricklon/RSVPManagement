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

## Installation & Setup

Step-by-step instructions on how to install and setup the system.
To install the project dependencies:

```shell
$ poetry install
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
