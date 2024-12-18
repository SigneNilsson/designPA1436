---
Title: Galleri
Description: This is our gallery page.
---

Signes galleri
==========================

Här visas ett fantastiskt bildgalleri:

<!-- <img src = "image/myimg.jpg?w=960&q=90" alt = "exempelbild">  -->
<!-- ?w=960 gör att maxbredd blir 960? frågetecknet skickar till? Cimage argumentet efter skickas alltså till cimage. & tecken gör att vi kan skicka flera argument. q står för quality är en skala på 0-100.-->
<div class = "gallery">

<a href="image/myimg.jpg">
    <picture class = "pic1">
        <source media="(min-width: 668px)" srcset="image/myimg.jpg?w=960&q=90">
        <source media="(min-width: 376px)" srcset="image/myimg.jpg?w=667&q=70">
        <img src="image/myimg.jpg?w=375&h=375&crop-to-fit&q=70" alt="exempelbild">
    </picture>
</a>

<a href="image/santas.jpg">
    <picture class = "pic2">
        <source media="(min-width: 668px)" srcset="image/santas.jpg?w=960&q=90">
        <source media="(min-width: 376px)" srcset="image/santas.jpg?w=667&q=70">
        <img src="image/santas.jpg?w=375&h=375&crop-to-fit&q=70" alt="exempelbild">
    </picture>
</a>


<a href = "image/snowman.jpg">
    <picture class = "pic3">
        <source media="(min-width: 668px)" srcset="image/snowman.jpg?w=960&q=90">
        <source media="(min-width: 376px)" srcset="image/snowman.jpg?w=667&q=70">
        <img src="image/snowman.jpg?w=375&h=375&crop-to-fit&q=70" alt="exempelbild">
    </picture>
</a>

<a href="image/santa2.jpg">
    <picture class = "pic4">
        <source media="(min-width: 668px)" srcset="image/santa2.jpg?w=960&q=90">
        <source media="(min-width: 376px)" srcset="image/santa2.jpg?w=667&q=70">
        <img src="image/santa2.jpg?w=375&h=375&crop-to-fit&q=70" alt="exempelbild">
    </picture>
</a>

</div>

En youtube-klassiker:
<div class="embed-container">
    <iframe src="https://www.youtube.com/embed/jNQXAC9IVRw?si=ZaWcvUvK9bra1MmW" title="Youtube classic: me at the zoo" frameborder="0" allowfullscreen></iframe>
</div>

<!-- kan bestämma att vissa delar av bilden ska kapas när den blir mindre så att de t.ex. blir högra halvan bara. se cimage crop. -->