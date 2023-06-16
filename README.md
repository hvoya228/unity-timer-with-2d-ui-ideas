# Timer script explaining and UI ideas preview

![UI Example Image](https://github.com/chugaister228/UnityTimer/blob/main/Prewiews/AllUiVideoPrewiev.gif)
All UI implementations are working with one timer, but you can make more.  

---  

### How to use  
Create empty GameObject and attach *Timer.cs* script, paste the seconds duration float in the inspector.  
By default :hourglass: is 300f (5 min).
  
Now you can use Timer in any file: *[SerializeFiled] private Timer timer*;   
Base methods: *timer.StartTimer(), timer.StopTimer(), timer.ContinueTimer()*.  

You can also implement singletone patter to use only one timer in your game.  

UI implementations have two scripts - *TimerText.cs* and *TimerProgress.cs*  
(to make reverse progress click isReverse in the Inspector)  

All UI implementations are working without dependencies.  
Events work instead of dependencies to optimize the Timer and SOLID following.  

---

### Other features  
Properties:  
*timer.Duration* - returns general time to time over  
*timer.TimeRemaining* - returns time left to time over  
*timer.IsTimeOver* - returns true if time is over  

Methods:    
*timer.IsMoreThanSomeTimeLeft(float time)* - returns true if time remaining is more than given time  
*timer.IsLessThanSomeTimeLeft(float time)* - returns true if time remaining is less than given time  

Events:  
*Timer.OnTimerStart* - static event which can be signed on some void method and will be invoked when time is starting decreasing  
*Timer.OnTimerWorking* - static event which can be signed on some void method and will be invoked when time is decreasing  
*Timer.OnTimerFinish* - static event which can be signed on some void method and will be invoked when time is over   

---  

git pull the project to see how it works