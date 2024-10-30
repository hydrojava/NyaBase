# NyaBase
A base for minecraft bukkit plugin made in Kotlin.

## Command
````kotlin
object ExampleCommand :
    CommandBase(
        "example",
        "server.command.example",
        false,
        true,
        "Example Command",
        "exam", "exp"
    ) {
    override fun execute(sender: CommandSender, args: Array<out String>) {
        TODO("Not yet implemented")
    }
}
````

## EventListener
````kotlin
class ExampleListener : EventListener(ListenerPriority.NORMAL, listOf(PacketType.Play.Client.CHAT)) {
    init {
        onPacketReceive {
            TODO("On packet receiving runs")
        }
    }

    @EventHandler
    fun onQuit(event: PlayerQuitEvent) {
        TODO("Other bukkit event listener")
    }
}
````

## Tasks
````kotlin
object ExampleTask : AbstractTask(10, async = true) {
    override fun run() {
        TODO("Task runs loop")
    }
}
````
