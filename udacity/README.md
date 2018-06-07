# Links
- http://udacity.github.io/60fps/lesson1/layoutPaint/index.html
- https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/timeline-tool?utm_source=dcc&utm_medium=redirect&utm_campaign=2016q3#rendering-event-properties
- https://csstriggers.com/
- https://github.com/udacity/devsummit/blob/master/src/static/scripts/components/card.js
- https://speakerdeck.com/paullewis/making-a-silky-smooth-web



# Frames
- 1000ms
- **60 Hz** or **60 fps**
- 1000ms / 60fps = **16ms**
  
> We usually round down to **16ms per frame**

## Making Frame
1 - Receive the DOM
!(DOM)[https://i.imgur.com/b7UpNPj.png]
2 - Receive the CSS
!(CSS)[https://i.imgur.com/UYdHWkC.png]
3 - Combine DOM + CSS | Called **RECALCULATE STYLES
!(Recalculate Styles)[https://i.imgur.com/S8etRCp.png]
4 - Generate the **Render Tree**
    - Remove scripts
    - Remove hide elements
    - Added pseudo-element 
!(Render Tree)[https://i.imgur.com/CJuRhZK.png]
!(Remove Elements)[https://i.imgur.com/TOqGCel.png]
!(Add pseu elements)[https://i.imgur.com/4zhV4kN.png]


## Three ways Pipeline

1 - Visual change with CSS or Javascript 
!(Visual change with CSS or Javascript)[https://i.imgur.com/6yqViLQ.png]
2 - Change paint property: eg: backgroud, color, text shadow
!(Change paint property)[https://i.imgur.com/9ThmEI3.png]
3 - Just composite
!(Just composite)[https://i.imgur.com/qjbQrlW.png]


# LIFE CYCLE WEB

## RAIL
> **R**esponse **A**nimations **I**dle **L**oad
!(RAIL)[https://i.imgur.com/NSGbfqU.png]

# PATTERN

## FLIP
> **F**irts **L**ast **I**nvert **P**lay
- Firts | Where is element start
- Firts | Where is element ended

# Examples
!(Interactions and Animations)[https://i.imgur.com/QJY2mhy.png]

!(Times)[http://udacity.github.io/60fps/images/time-table.jpg]

# Observations
- Frames
  - Browser need 10ms to 12ms
- Render Tree
  - Elements that are display: none don't show up in the Render Tree
- Three ways Pipeline
  - **Flexbox** dont modify the **style**
- **Opacity** and **transform** only trigger **composite**