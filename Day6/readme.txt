1.By default sare object ki position default STATIC hoti hai.
2.lekin hm objects ki position ko change kar sakte hai...
LIKE position:relative 
ab relative positioning hame 4 functionalities provide karti hai i.e
{top,bottom,left,right}
top:20px;
likhne se jo object hai apne original
position ke relative me niche move kar jata hai 10px.
left:20px;
iska matlab hai object apne original position
se 20px left move karega.
Relative apne original position ke respect me 
left right top bottom move karta hai....
relative positioning me object ke originalposition par koi aur nahi aa sakta hai.

NEXT POSITION IS ABSOLUTE.

absolute apna original position leave kar deta hai.
wo space occupy nahi karta apna so us space 
ko koi aur bhi le sakta hai.
ab absolute me left,right ,top,bottom karne par 
kiske relative me move karta hai objecrt.
top:20px;
kyaa viewport ke relation me move kar rha nahi....
1. sabse pehle ye apne parent element ko dekhta hai
aur parent element me dekhta hai ki kya koi uska position fix hoo rakha hai..
agar koi position specify nahi hai..
aur by default static rehta hai fir position tab ignore karta hai apne parent element ko
2. ab dekhta hai wo apne parent ke parent koo ...
hamare case me box2 div ka parent div container hai.
aur usme position specify nahi hai too ab div container ka parent ko dekhege 
jo ki hai body!
YAHA par bhi position mention nahi hua hai..
too ab object vieport ke basis par apni position 
ko shift karega.
lekin agar iske parent element 
div container par position relative daal du
too ye apni position ko parent element ke respect me change karega.


NEXT AB HAM FIXED POSITION KE BARE ME PADHEGE

  fixed hamesha apna position find karega viewport ke basis par 
  aur ye object fixed ho jata hai us position par
  navbar create karne ke liye use karte hai isko ham.
  fixed bhi apna position leave kar deta hai us spac ko koi aur 
  object occupy kar sakta hai.
    

    NEXT HAI STICKY POSITION

    sticky bhi fixed ho jata hai 
    lekin wo jis parent element ke 
    ander stick hai usi me fixed hoga aage
    dusre elements me nahi fixed hoga 

    Bahut common confusion hai. Sticky ko samajhne ke liye ek rule yaad rakho:

position: sticky tab tak kaam nahi karta jab tak tum offset (top, left, right, ya bottom) define na karo.

Tumhara code:
.box {
    position: sticky;
    top: 10px;
}
Agar top na likho:
.box {
    position: sticky;
}

To browser ko pata hi nahi chalega ki kab sticky hona hai. Isliye element normal position: relative ki tarah behave karega.

top: 10px likhne ke baad bhi effect kyu nahi dikh raha?

Iske kai reasons ho sakte hain:

1. Scroll hi nahi ho raha

Agar page ki height viewport se chhoti hai to sticky kabhi activate nahi hoga.

Example:

body{
    height: 200vh;
}

Ab scroll hoga aur sticky ka effect dikhega.

2. Sticky element shuru se hi top par hai

Agar element pehle se hi top ke paas hai, to top:10px ka difference bahut kam dikhega.

Example:

header{
    position: sticky;
    top:10px;
}

Ye scroll karte hi viewport ke top se 10px niche chipak jayega.

3. Parent element ki height kam hai

Sticky sirf apne parent container ke andar hi kaam karta hai.

<div class="parent">
    <div class="box"></div>
</div>

Agar .parent ki height bahut kam hai, to sticky ka effect properly nahi dikhega.

4. Parent par overflow: hidden, overflow: auto, ya overflow: scroll laga hai

Ye sticky ko affect kar sakta hai.

.parent{
    overflow:hidden;   /* Sticky issue ho sakta hai */
}
top:10px ka actual matlab
Scroll Start

----------------------
|                    |
|  Box               |
|                    |
----------------------

Scroll Down

10px
↓
----------------------
|                    |
|  Box  ← yahan chipak jayega
|                    |
----------------------

Matlab viewport ke top se 10px niche box ruk jayega.

Interview/Exam Point
position: sticky = Relative + Fixed ka combination.
Jab tak scroll threshold (top, left, right, bottom) cross nahi hota, element normal rehta hai.
Threshold cross hote hi element viewport ke respect me fixed ho jata hai.
Isliye top, left, right, ya bottom me se kam se kam ek property dena zaroori hota hai.