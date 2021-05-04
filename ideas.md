# Performance

## Use main thread for UI work only

Move the Redux logic into a webworker and keep two stores synced with Immer and patches. Allowing the main thread to ship frames while redux is working.

## Create an optimized path for each action type

Instead of running every reducer for each action we mutates the root reducer the first time it sees an action of that type.
