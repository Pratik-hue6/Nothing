# Nothing
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Deeya!</title>
<style>
  body {
    background-color: black;
    color: #00ff00;
    font-family: monospace;
    white-space: pre;
    padding: 20px;
  }
  .firework {
    text-align: center;
    font-size: 18px;
    line-height: 1;
  }
  .cake {
    text-align: center;
    font-size: 18px;
    margin-top: 20px;
  }
  .message {
    color: #ffffff;
    font-size: 16px;
    margin-top: 20px;
  }
</style>
</head>
<body>

<div id="output"></div>

<script>
const output = document.getElementById('output');

// 🎆 Fireworks frames
const fireworks = [
`        *        \n       ***       \n      *****      \n     *******     \n      *****      \n       ***       \n        *        `,
`        *        \n       ***       \n      *****      \n     *******     \n      *****       \n       ***       \n        *        `
];

// 💚 Hacker-style terminal text
const hackerText = [
">>> Loading Celebration Module...",
">>> Initializing Deeya Birthday Protocol...",
">>> Setting Happiness = 100%",
">>> Activating Fun Mode 🎉",
">>> Get Ready! 🎂"
];

// 🎂 ASCII Cake
const cake = [
"       i i i i i       ",
"      |:H:a:p:p:y:|      ",
"    __|___________|__    ",
"   |^^^^^^^^^^^^^^^^^|   ",
"   |:B:i:r:t:h:d:a:y:|   ",
"   |                 |   ",
"   |      Deeya      |   ",
"   |                 |   ",
"   ~~~~~~~~~~~~~~~~~~~   "
];

// Full birthday message
const message = `Happy Birthday Deeya! 🎉🎂 Wishing you a very amazing and happy birthday.
May your day be filled with lots of happiness, good moments, and positive vibes.
I hope this new year of your life brings you success, good health, and many great opportunities.
Keep smiling, keep enjoying life, and keep doing the things you love.
May all your goals and dreams come true and may you always stay happy and confident.
Enjoy your special day with your friends and family and make lots of great memories.
Once again, happy birthday and have a wonderful year ahead! 🎁✨`;

async function sleep(ms) {
  return new Promise(resolve => setTimeout(resolve, ms));
}

// Fireworks animation
async function showFireworks() {
  for (let i = 0; i < 3; i++) {
    output.innerHTML = '<pre class="firework">' + fireworks[i % 2] + '</pre>';
    await sleep(200);
    output.innerHTML = '';
    await sleep(100);
  }
}

// Hacker terminal animation
async function showHackerText() {
  for (const line of hackerText) {
    output.innerHTML += '<pre class="firework">' + line + '</pre>';
    await sleep(400);
  }
  await sleep(200);
  output.innerHTML = '';
}

// ASCII cake animation
async function showCake() {
  for (let i = 0; i < 3; i++) {
    output.innerHTML = '<pre class="cake">' + cake.join('\n') + '</pre>';
    await sleep(300);
    output.innerHTML = '';
    await sleep(100);
  }
}

// Typing-style birthday message
async function showMessage() {
  let html = '<pre class="message">';
  for (const char of message) {
    html += char;
    output.innerHTML = html + '</pre>';
    await sleep(10);
  }
  output.innerHTML += '\n\n🎉🎂💚 ALL THE BEST, DEEYA! 💚🎂🎉';
}

// Run all animations
async function celebrate() {
  await showFireworks();
  await showHackerText();
  await showCake();
  await showMessage();
}

celebrate();
</script>

</body>
</html>
