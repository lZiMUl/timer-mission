# timer-mission

install the dependency:
```
npm install timer-mission --save
```

### use the instance. 
```js
'use strict';

// import dependency
import TimerMission from 'timer-mission';

// setting event
const timerMission = new TimerMission([{
  "event": "goToWork",
  "timer": "6:15:0"
}, {
  "event": "goOffWork",
  "timer": "22:30:15"
}]);

// monitor event
timerMission.addEventListener('goToWork', function () {
  console.log(...arguments);
});

timerMission.addEventListener('goOffWork' function () {
  console.log(...arguments);
});
```

## or use class
```js
'use strict';

// import dependency
import TimerMission from 'timer-mission';

// definition method class
class Demo extends TimerMission {
  constructor() {
    super(...arguments);
    // monitor event
    super.addEventListener('goToWork', function () {
      console.log(...arguments);
    });
    super.addEventListener('goOffWork' function () {
      console.log(...arguments);
    });
  }
};

new Demo([{
  "event": "goToWork",
  "timer": "6:15:0"
}, {
  "event": "goOffWork",
  "timer": "22:30:15"
}]);
```