

A. From client to browser

1. signup to the server
  input: {
    cmd: 'signup',
    name: <player's name>,
    email: <player's email address>,
    password_hash: <hash of password>,
  }

2. Login to the server
  input: {
    cmd: 'login',
    email: <player's email address>,
    password_hash: <hash of password>,
  }
  output: {
    error: <error message>,
    player_id: <player_id>,
  }

3. Get the available room list
  input: {
    cmd: 'get_room_list',
  }
  [pull and push]
  output: {
    error: <error message>,
    rooms: [    
      {
        room_id: <room_id>,
        players: [
          {
              name:
          },
        ],
      },
      {
        room_id: <new_room_id>,
      }
    ]     
  }

4. join a room
  input: {
    cmd: 'join_room',
    room_id: <room_id>    
  }
  output: {
    error: <error message>,
  }

5. leave the room
  input: {
    cmd: 'leave_room',
    room_id: <room_id>    
  }
  output: {
    error: <error message>,    
  }

6. start game (from server to client)
  input: {
    cmd: 'start_game',
    room_id: <room_id>    
  }
  output: {
    error: <error message>,
    player_ids: [player's list],
  }


8. Choose a game
  input: {
    cmd: 'choose_game'
    game_id: ''
  }

9. Enter the game


B. From client to client

1.
