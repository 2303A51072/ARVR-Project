# Pathfinder AR Campus Navigator

A mobile-friendly student prototype that helps campus visitors choose a destination, view a walking route, and follow an augmented reality style camera guide.

## Run the project

Open index.html in a modern browser to try the interactive campus map and route planner. No package installation is needed.

To enable live camera mode, serve this folder from a secure browser context such as localhost or HTTPS. From the project folder, run:

    python -m http.server 8000

Then open http://localhost:8000 and allow camera access. A phone browser provides the clearest camera demonstration.

## Demo steps

1. Choose a starting point, such as North Gate.
2. Enter a destination such as Library, Science Lab, Cafeteria, Main Block, Auditorium, or Sports Complex. The popular destination buttons also work.
3. Select Find my route to draw the route and display walking directions and an estimated distance.
4. Turn on Camera guide to see the direction prompts over the live camera view.
5. Use the reset icon to clear the route.

## Project objective

New students and visitors can lose time looking for classrooms and campus facilities. This prototype demonstrates a simple mobile interface for finding a destination and following a suggested walking route.

## How it works

- The fictional campus is represented as a graph of landmarks connected by walkable paths.
- Dijkstra's shortest path algorithm finds a low-distance route between the selected locations.
- SVG draws the selected route on the campus map.
- The browser camera API provides a live video background for an HTML and CSS direction overlay.
- The layout adapts to smaller phone screens.

## Technology

HTML, CSS, JavaScript, SVG, browser media APIs, and a graph shortest path algorithm. The app has no build step or package dependencies.

## Limitations and future work

Greenfield Campus and the distances are sample data. The camera guide shows directions over the camera feed, but does not determine the user's location, track movement, or recognize buildings. A production campus navigator would need a real campus map, positioning data, accessible routes, and ARCore, ARKit, or WebXR based tracking.

Possible next steps include replacing the sample campus with a real campus map, adding room numbers and accessible paths, and integrating device positioning.

## Project files

- index.html contains the page and map layout.
- styles.css contains the responsive styling and camera overlay.
- app.js contains the campus graph, route algorithm, and camera controls.
- README.md contains setup and demonstration instructions.
