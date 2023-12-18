# wt-js-02-color-switcher-timer.
# Завдання 1 - перемикач кольорів
<button type="button" data-start>Start</button>
<button type="button" data-stop>Stop</button>
# Завдання 2 - таймер зворотного відліку​

<input type="text" id="datetime-picker" />
<button type="button" data-start>Start</button>

<div class="timer">
  <div class="field">
    <span class="value" data-days>00</span>
    <span class="label">Days</span>
  </div>
  <div class="field">
    <span class="value" data-hours>00</span>
    <span class="label">Hours</span>
  </div>
  <div class="field">
    <span class="value" data-minutes>00</span>
    <span class="label">Minutes</span>
  </div>
  <div class="field">
    <span class="value" data-seconds>00</span>
    <span class="label">Seconds</span>
  </div>
</div>

function convertMs(ms) {
    <const second = 1000;>
    <const minute = second> *<60;>
    <const hour = minute> * <60;>
    <const day = hour> * <24;>

    <const days = Math.floor(time / (1000 * 60 * 60 * 24));>
  <const hours = Math.floor((time / (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));>
   <const mins = Math.floor((time / (1000 * 60 * 60)) / (1000 * 60));>
  <const secs = Math.floor((time / (1000 * 60)) / 1000);>

  return { days, hours, minutes, seconds };
}

console.log(convertMs(2000)); // {days: 0, hours: 0, minutes: 0, seconds: 2}
console.log(convertMs(140000)); // {days: 0, hours: 0, minutes: 2, seconds: 20}
console.log(convertMs(24140000)); // {days: 0, hours: 6 minutes: 42, seconds: 20}
