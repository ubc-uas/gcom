# GCOM

## Overview

Welcome to the monorepo for the UAS Ground Communications project.
It houses the channel of communication between the drone and the web-app for waypoints, drone-actions and status updates.

It contains 3 main sub-projects:

1. **web-frontend** provides the user interface for operators
2. **web-backend** acts as the central server coordinating data flow and business logic
3. **mission-planner** handles low-level drone communication and flight operations
4. **integration-testing** provides integration testing for the connection between `mission-planner` and `web-backend`

Data flows from the drone through mission-planner → web-backend → web-frontend, with real-time updates pushed via WebSockets for live telemetry and status information.

The connection works like this:

- `mission-planner` interacts directly with the drone, and exposes a mavlink connection for interactions with the `web-backend`.
- The `web-backend` exposes a REST API for the `web-frontend` to communicate with.

## Projects Overview

Learn more about each project from their individual readmes:

**WIP**
