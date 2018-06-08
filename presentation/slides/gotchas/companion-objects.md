### Companion Objects

```
data class Team(val city: String, val name: String, var sport: Sport) {
    companion object {
        fun createBaseballTeam(city: String, name: String)
            = Team(city, name, Sport.Baseball)
    }
}
```

```
val cubs = Team.createBaseballTeam("Chicago", "Cubs")
```

Note:
+