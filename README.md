# PowerApps Conference Room Booking App

## Overview

The PowerApps Conference Room Booking App is a canvas application designed to streamline the process of booking conference rooms. This responsive application offers a user-friendly interface to view, book, and manage conference room reservations, ensuring a seamless experience across mobile and desktop devices.

## Features

- **Home Screen:** Displays today's bookings with an option to view all bookings.
- **New Booking Screen:** Allows users to book a new room with date and time restrictions to prevent booking past times.
- **Room Details:** Shows room capacity, available devices (audio, TV, projector), and other metadata.
- **Logout Option:** Provides a secure way to exit the application.
- **Enhanced User Experience:** Dynamic start and end times based on current system time, and only future dates and times are selectable.

## Technologies

- **PowerApps:** Canvas App for building the user interface and managing bookings.
- **Power Automate:** For integrating with Office 365 and managing room data.
- **Dataverse:** For storing room and meeting information.
- **Office 365 Outlook:** For fetching room details and creating calendar events.

## Data Sources

- **Dataverse Tables:**
  - `Conference Rooms`: Stores room details including capacity, devices, and metadata.
  - `Meeting Information`: Stores meeting details such as room, start time, end time, and organizer.
- **Office 365 Connectors:**
  - `O365 Outlook`: For managing calendar events and fetching room information.
  - `O365 Users`: For managing user information.

## Power Automate Flows

- **Get Meeting Rooms Flow:**
  - Fetches room email addresses and names from Office 365 resources.
  - Checks Dataverse table to avoid duplicate entries.
  - Adds new rooms to the Dataverse table with relevant metadata.

## Installation

1. **Import the Solution:**

   - Download the solution zip file provided.
   - Go to your PowerApps environment and click on `Import`.
   - Browse and select the solution zip file, then follow the prompts to complete the import.

2. **Configure the App:**

   - Ensure that all necessary connectors (Office 365 Users, Outlook) are set up.
   - Run the `Get Meeting Rooms Flow` to fetch and update room details from Office 365.
   - Verify that the Dataverse tables (`Conference Rooms` and `Meeting Information`) are correctly populated with initial data.

3. **Publish the App:**
   - Open the imported app in PowerApps Studio.
   - Make any necessary adjustments to the settings and publish the app.

## Usage

1. **Booking a Room:**

   - Open the app and navigate to the `New Booking` screen.
   - Select the desired date, start time, and end time.
   - Choose an available room from the list, optionally provide meeting details, and complete the booking.

2. **Viewing Bookings:**

   - On the home screen, view today's bookings or click `View All` to see all upcoming bookings.

3. **Managing Room Details:**
   - Admins can use the `Conference Rooms` Dataverse table to update room metadata, such as capacity, available devices, images, etc.

## Support

For any questions or issues, please contact me [LinkedIn](https://www.linkedin.com/in/swaminawale/) or [YouTube](https://www.youtube.com/@PowerPlatformSimplified).
