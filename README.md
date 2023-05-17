# Game-Lobby

Game Lobby is a part of the Spichki Game project. This microservice provide gPRC API (see [proto](url)).


<br>
<br>


# Data model


#### Headers hashmaps:
```ruby
header:1001  ->  {status: "FULL", max_players: 2}
header:1002  ->  {status: "OPEN", max_players: 3}
header:1003  ->  {status: "PLAY", max_players: 4}
header:1004  ->  {status: "OPEN", max_players: 4}
header:1005  ->  {status: "PLAY", max_players: 6}

```

#### Status sets:
```yaml
status:OPEN  ->  {1002, 1004}
status:FULL  ->  {1001}
status:PLAY  ->  {1005, 1003}

```

#### Max players sets:
```yaml
max_players:2   ->  {1001}
max_players:3   ->  {1002}
max_players:4   ->  {1003, 1004}
max_players:5   ->  (nil)
max_players:6   ->  {1005}
max_players:7   ->  (nil)
max_players:8   ->  (nil)
max_players:9   ->  (nil)
max_players:10  ->  (nil)

```

#### Group sets:
```yaml
group:1001  ->  {1001, 1006}
group:1002  ->  {1002}
group:1003  ->  {1003, 1008, 1013}
group:1004  ->  {1004, 1009}
group:1005  ->  {1005, 1010, 1015, 1017}

```

#### Join players set:
```yaml
players:JOIN  ->  {1006, 1008, 1013, 1009, 1010, 1015, 1017}

```
