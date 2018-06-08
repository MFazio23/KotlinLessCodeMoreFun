### Null Safety
#### Safe Calls

```
val brewers: Team? = Team("Milwaukee", "Brewers", Sport.Baseball)
val whiteSox: Team? = Team("Chicago", "White Sox", Sport.Baseball)
val devilRays: Team? = null

val teams = listOf(brewers, whiteSox, devilRays)
```

```
val nicknames: List<String?> = baseballTeams.map {
    if (it != null) it.name else ""
}
```

```
val nicknames: List<String?> = baseballTeams.map {
    it?.name ?: ""
}
```


Note:
+