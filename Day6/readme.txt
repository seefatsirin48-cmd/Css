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
    