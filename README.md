# Honored-mapusaurus
Thank you very much #つぶやきProcessing

![buh](https://github.com/nicolasbaez/Honored-mapusaurus/blob/main/xp040.gif)
```javascript
setup = (_) => createCanvas((w = 500), w);
k = 0;
draw = (_) => {
  background(0);
  for (i = 0; i <= w; i += 3)
    for (j = 0; j <= w; j += 3) {
      noStroke();
      fill(map(noise(i * 0.01, j * 0.01, k), -0.1, 0.6, 0, 255));
      rect(i, j, 2, 2);
    }
  stroke(random(128));
  noFill();
  strokeWeight(4);
  ellipse(250, 200, 150);
  if (k == 0) saveGif("xp040.gif", 1024, { delay: 0, units: "frames" });
  k += 0.005;
};
