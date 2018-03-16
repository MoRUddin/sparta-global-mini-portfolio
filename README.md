# sparta-global-mini-portfolio
This project was built in html and css. The project was designed to be an introductory look at webpage design, spacing, and responsiveness (to different screen sizes.)

## i) Structure
The website is comprised of many container `<div>`s with content being held within these. These were used in conjunction with `flex` to make a dynamic, responsive website.

## ii) Positioning and alignment
Alignment was achieved within css by applying the following to relevant containers.
```css
html,body{
  text-align: center;
}
```
as well as
```css
.parent{
  display: flex;
  flex-direction: column/row;
}
.child{
  flex: <ratio>;
}
```
The former was used to center generic objects, (which would be inherited by div to center align images and containers). Flex boxes were used to position containers and containers within containers; to equate containers in height, size containers proportionally (using `<ratio>`), and to direct the order of stacking (in rows or columns.)

Flex also provided a solution to slightly more complicated spacing problems, the main example being on the navbar. By setting the logo and list of links as the flex children
```css
.parent{
  justify-content: space-between;
}
```

## ii) Responsiveness
This was implemented through a media query dependent on the screen size:
```css
@media (maximum-width: 768px) {
  .parent{
    flex-direction: row;
  }
  .child1{
    flex: 1;
  }
  .child2{
    flex: 1;
  }
}
```
This told the flex parent container to order the child objects vertically upto a screen size of 768 pixels wide.

Any images used within the webpage were styled with `max-width` percentages, so they would automatically scale with the page.

**Muhammad-Rayhaan Uddin**
>Mini Portfolio
