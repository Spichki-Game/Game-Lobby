# Game-Lobby

Game Lobby is a part of the Spichki Game project. This microservice provide gPRC API (see [proto](url)).


<br>
<br>


# Data model


#### Headers hashmaps:
```shell
header:1001  ->  {status: 'OPEN', max_players: 3}
header:1002  ->  {status: 'FULL', max_players: 2}
header:1003  ->  {status: 'FULL', max_players: 5}
header:1004  ->  {status: 'OPEN', max_players: 8}
header:1005  ->  {status: 'PLAY', max_players: 5}

```

#### Status sets:
```yaml
status:OPEN  ->  {1003, 1005}
status:FULL  ->  {1001, 1002}
status:PLAY  ->  {1004}

```

#### Max players sets:
```yaml
max_players:2   ->  {1002}
max_players:3   ->  {1001}
max_players:4   ->  {1003, 1005}
max_players:5   ->  {1004}
max_players:6   ->  {1004}
max_players:7   ->  {1004}
max_players:8   ->  {1004}
max_players:9   ->  {1004}
max_players:10  ->  {1004}

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
