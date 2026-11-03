# Lottery Draw / Losziehung

A single-file web app for drawing lottery tickets by color and number. No build step, no dependencies.

## Features

- Setup: any number of colors, each with its own name, color and number range (e.g. Red 1–500, Blue 1–300)
- Draw screen with fullscreen mode; every remaining ticket has the same chance (Web Crypto random numbers)
- Drawn tickets are removed from the pool
- Draw animation, can be switched off; length adjustable from 0.5 to 10 seconds
- Ticket width on the draw screen adjustable from 30 % to 95 % of the screen width; the text scales with it (the box is also capped so it always fits the screen height)
- Draw history, undo last draw, reset pool
- German / English, picked automatically from the browser language and switchable
- State saved in `localStorage`, so it survives browser restarts
- Light and dark mode follow the system setting

## Notes

- Saved state lives in the browser on that device only. Clearing site data, or a private window, starts fresh.
- While tickets have been drawn, the setup is locked. Reset the pool to change colors or ranges.
- Safari on iOS only partially supports the Fullscreen API. If a browser doesn't offer it, the fullscreen button is hidden and the draw screen still fills the browser window.
