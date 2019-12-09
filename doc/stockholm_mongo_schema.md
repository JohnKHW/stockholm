
players
  player_id
  email
  pwd_hash
  name
  win
  lose

roles[
  {
    role_id
    names    
  }
]


games
  game_id
  players: [
    {
      player_id
      role
    }
  ]
