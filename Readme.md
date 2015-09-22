## Liars Dice Backend TEST
#### A simple imperfect node backend for UI engineer interviews

## Setting up

1. Clone the repository locally
2. Make sure you have Node installed (https://nodejs.org/download/)
3. Run npm install
4. node index.js

The server will run on localhost:8080

## See it in action

There is a Postman collection included test/LiarsDice.json.postman_collection. This file can be loaded into the Chrome app, Postman and demonstrates usage of all the endpoints.

## Endpoints

Start a new game

```
POST /games
  numPlayers: Integer
  numDice: Integer
```

Get a single game

```
GET /games/:id
```

List Games

```
GET /games
```

On a users turn, they can either make a claim and move dice to the middle, or challenge the previous player.

Make a claim

```
POST /games/:id/claim
  player: Integer
  moveNumber: Integer
  moveFace: Integer
  claimNumber: Integer
  claimFace: Integer
```

Challenge the last move

```
POST /games/:id/challenge
  player: Integer
```
