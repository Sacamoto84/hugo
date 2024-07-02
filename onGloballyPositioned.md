```kotlin
 var sizeTopBar by remember { mutableStateOf(IntSize.Zero) }
 var positionInRootTopBar by remember { mutableStateOf(Offset.Zero) }

 TopAppBar(
        modifier = Modifier
          .onGloballyPositioned { coordinates ->
             // size
             sizeTopBar = coordinates.size

             // global position (local also available)
             positionInRootTopBar = coordinates.positionInRoot() 

          }
       //...
 )
```
