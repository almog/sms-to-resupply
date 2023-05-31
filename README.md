# What's here
A service that lets me to place orders using a Garmin InReach satellite messenger or really any form of communication that can message a predefined number / email address.

# Background

When I hiked the Pacific Crest Trail few years ago, I used to order items that needed to be replaced or that I lost to the next or town stop using my phone (most towns have a general store or a supermarket, often not an outfitter).

However, it's not uncommon for sections of the trail to be outside cell service for days between town to the next one.

Anyhow, since the next trail that I plan to hike, the Continental Divide Trail, is even more remote than the PCT, I started to play with a prototype of a satellite messenger backed service to let me order items from a predefined list (each can match multiple items of a different priority) and be shipped to a predefined shipping address (post offices of trail towns along the trail).

# How should it work
Assuming that one of my contacts is a phone number that my service is monitoring, I can text a message like so:

  items: shoes, tape, filter, usb cable, ice axe;
  to: Chama;
  eta: 2023-07-01;

The service should place an order of a predefined pair of shoes, water filter, Leukotape and USB cable and ice axe to Chama, NM. Messages are limited to 160 characters before they get split, and so to keep it simple, I might use shorter abbreviations for some items.

If any item on the list can't be delivered until 2023-07-01 using prime shipping (unfortunately it's the easiest option), it should be dropped from the order. Alternatively, if the guaranteed delivery date is off by 1 day, I might just place it on a separate order, hope for the best and if it doesn't show up on time, it'll get returned individually after not being claimed. 
