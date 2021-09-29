HTML markup:
header>article#box$*10>(h2>lorem5)+p>lorem7


CSS hint:
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

header {
  max-width: 1630px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
  grid-template-rows: repeat(4, minmax(250px, 1fr));
  grid-template-areas:
    "box1 box1 box2 box3 box3"
    "box1 box1 box4 box5 box5"
    "box6 box7 box7 box5 box5"
    "box6 box8 box9 box9 box10";
  gap: 20px;
}

article {
  background-color: #ddd;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  padding: 1em;
}

#box1 {
  grid-area: box1;
}

#box2 {
  grid-area: box2;
}

#box3 {
  grid-area: box3;
}

#box4 {
  grid-area: box4;
}

#box5 {
  grid-area: box5;
}

#box6 {
  grid-area: box6;
}

#box7 {
  grid-area: box7;
}

#box8 {
  grid-area: box8;
}

#box9 {
  grid-area: box9;
}

#box10 {
  grid-area: box10;
}

@media screen and (max-width: 768px) {
  header {
    grid-template-columns: 1fr 1fr;
    grid-template-rows: repeat(6, minmax(200px, 1fr));
    grid-template-areas:
      "box1 box2"
      "box3 box4"
      "box5 box5"
      "box6 box7"
      "box8 box9"
      "box10 box10";
  }
}

@media screen and (max-width: 700px) {
  header {
    grid-template-columns: 1fr;
    grid-template-rows: repeat(10, minmax(150px, 1fr));
    grid-template-areas:
      "box1"
      "box2"
      "box3"
      "box4"
      "box5"
      "box6"
      "box7"
      "box8"
      "box9"
      "box10";
  }
}
