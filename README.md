# hugo
# Заголовок первого уровня #

### Заголовок третьего уровня ###

###### Заголовок шестого уровня ######

```kotlin
import java.util.Calendar  
import java.util.Date

//Version 1.0.0 Занесена в гримуар 05.04.2024

/**  
 * Получить дату начала текущих суток
 */
 fun getStartDayNow(offsetDay : Int = 0): Date  
{  
    //    val date = Date()  
    //  
    //    // Устанавливаем время в полночь (начало суток)  
    //    date.hours = 0  
    //    date.minutes = 0  
    //    date.seconds = 0  
    //    date.setTime(date.time - (date.time % (24 * 60 * 60 * 1000  * (offsetDay + 1) ))) // Обнуляем миллисекунды  
  
    // Получаем текущую дату и время    val currentDate = Date()  
  
    // Устанавливаем время в полночь (начало суток)  
    val calendar: Calendar = Calendar.getInstance()  
    calendar.setTime(currentDate)  
    calendar.set(Calendar.HOUR_OF_DAY, 0)  
    calendar.set(Calendar.MINUTE, 0)  
    calendar.set(Calendar.SECOND, 0)  
    calendar.set(Calendar.MILLISECOND, 0)  
  
    calendar.add(Calendar.DAY_OF_YEAR, offsetDay)  
    // Получаем начало текущих суток  
    val startOfToday: Date = calendar.time  
    System.out.println("Начало текущих суток: $startOfToday")  
    return startOfToday  
}
```
