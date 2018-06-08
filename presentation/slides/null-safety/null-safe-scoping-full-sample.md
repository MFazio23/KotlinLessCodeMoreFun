### Null Safe Scoping

```kotlin
fun listTeams() {
    val brewers: Team? = Team("Milwaukee", "Brewers", Sport.Baseball)
    val whiteSox: Team? = Team("Chicago", "White Sox", Sport.Baseball)
    val devilRays: Team? = null

    println(this.getSummary(brewers))
    println(this.getSummary(whiteSox))
    println(this.getSummary(devilRays))
}
```
```kotlin
private fun getSummary(team: Team?): String {
    var fullName: String = "N/A"

    team?.let({t -> fullName = "${t.city} ${t.name} (${t.sport})"})

    return fullName
}
```

Note:
+