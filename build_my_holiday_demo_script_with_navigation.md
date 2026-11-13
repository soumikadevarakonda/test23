# Build My Holiday: demo script with navigation

*Written for you, recording the demo. Each step has **Navigate** (what
to click, using the exact labels on screen) and **Say** (what to read
out).*

## Before recording

1.  Run `database/seeds/demo_reset.sql`. Note that it deletes all saved
    trips and bookings.
2.  Start the backend (`uvicorn app.main:app --reload` in `backend/`)
    and the frontend (`npm run dev` in `frontend/`).
3.  Open http://localhost:5173.

## 1. Opening

**Navigate:** the home page, scrolled to the top.

**Say:** "This is Build My Holiday. Instead of booking flights, hotels,
transfers and activities separately, I can plan my whole holiday in one
place. Let me plan a trip for my family --- two adults and our
six-year-old --- from Bengaluru to Japan."

## 2. Search

**Navigate:**

1.  **Leaving from:** Bengaluru (BLR). **Going to:** Japan.
2.  **Start date:** 10-04-2027. **Nights:** 6.
3.  Click **Travelers**. Set Adults to 2, press **+** next to Children,
    choose **Child 1 age: 6 years**, then click **Done**.
4.  **Total budget:** 3,50,000.
5.  Point at the line **Or describe your trip in one line** (no need to
    use it).
6.  Make sure **Compare 3 options: cheapest, fastest and best rated** is
    ticked, then click **Search**.

**Say:** "I enter Bengaluru to Japan, starting 10 April for six nights.
I add two adults and one child with their age, and my budget of three
and a half lakh. I could also type the whole trip in one line here, and
the search fills itself in. I keep 'Compare 3 options' ticked and click
Search."

## 3. Recommended packages

**Navigate:** the page scrolls to **Pick your trip**. Move the mouse
across the three cards: **Cheapest**, **Fastest**, **Best rated**. Then
click **Choose** on the card you want. **Best rated** is the most
interesting to show.

**Say:** "I now see three recommended packages: the cheapest, the
fastest with the least travel time, and the best rated with the best
hotels within my budget. Each shows the cities, travel time, hotel
stars, total price and how it compares to my budget. I'll choose the one
that suits my family best."

## 4. Package details

**Navigate:**

1.  Point at the blue strip at the top (route, dates, travelers) and the
    **← Back to your 3 options** link.
2.  Point at **Price summary** on the right (total, budget bar).
3.  Scroll slowly through Day 1 to the last day.
4.  In **Search your trip**, type a hotel name or "temple", then clear
    it.
5.  Click the **Flights** filter, then **Everything**, then a **Jump to
    Day 3** link.

**Say:** "When I choose a package, I see all its details. At the top is
my trip summary, and I can go back to the three options anytime. On the
right, the price summary shows my total and how much budget is left.

Below is my day-by-day plan: the flight in, the airport transfer, the
hotel, activities on each day, and the flight home. I can search inside
my trip or filter to just flights, stays or activities, or jump to a
day. Every part is checked against the travel rules, so everything fits
together."

## 5. Making changes

**Navigate:**

1.  **Flight:** on Day 1, click **Change flight**. Point at the price
    differences, click **Select** on another flight, and point at the
    green **Your trip was updated** box.
2.  **Hotel:** on the hotel card, click **Change hotel**. Change **Sort
    by** to *Guest rating*, tick **Free cancellation only**, then click
    **Select** on a hotel.
3.  **Activities:** under a day, click **Add an activity on day 2** and
    then **Add** on one. On another activity, click **Remove**.
4.  **City split:** scroll to **Try a different city split** and point
    at it.
5.  **Undo:** at the top, click **Undo last change**.

**Say:** "I can change anything. When I change a flight, I see the price
difference first, and the app adjusts my airport transfer to match the
new time. I can change a hotel by sorting by price or rating, or picking
free cancellation. I can add or remove activities, choose a different
split of nights between cities, and undo any change."

## 6. Packing and weather tips

**Navigate:** scroll to the bottom of the trip to **Before you go**.
Point at **Weather in April**, **Good to know in Japan**, **For your
plans** and **For your group**, then click **Copy list**.

**Say:** "At the bottom, 'Before you go' gives me tips for this exact
trip: the usual April weather in each city and what to wear, things to
know about Japan like plug adapters and carrying cash, what to pack for
our activities, and tips for travelling with a child. I can copy it all
as a packing list."

## 7. Booking and the reservation number

**Navigate:**

1.  Click **Book this trip** in the price summary.
2.  In **Enter your details**, fill in Full name (e.g. *Rohan Menon*)
    and Email, then click **Book now**.
3.  On **Your trip is booked!**, point at the **Booking number** and
    click **Copy**. Then point at **Print** and **Download trip**.

**Say:** "I click 'Book this trip', enter my name and email, and
confirm. My whole holiday is booked, and I get one ten-digit reservation
number for everything. This number is my key to the booking. I can copy
it, print my confirmation or download the trip."

## 8. Using the reservation number

**Navigate:**

1.  Click **Find a booking** in the top header.
2.  Paste the number into **Find your booking**, then click **Find
    booking**. The trip opens.
3.  Scroll down the trip a little.
4.  In **Look up another booking**, type `1234567890`, then click **Find
    booking**. **Reservation not found** appears.

**Say:** "Later, I click 'Find a booking' at the top, enter my ten-digit
reservation number and click 'Find booking'. My complete trip opens
again, with every flight, hotel and activity and the price I paid, even
after the app has restarted. If I enter a wrong number, it tells me the
reservation was not found."

## 9. When things don't fit

**Navigate:**

1.  **Budget too small:** click **Plan a trip**. Use the same search but
    with **Total budget** 50,000, then click **Search**. The **This trip
    doesn't fit your budget** box appears.
2.  **No trip possible:** Chennai (MAA) → United Arab Emirates, **Start
    date** 08-04-2027, **Nights** 4, 4 adults + 4 children, budget
    6,00,000, then **Search**. The **No trip available for this search**
    box appears.
3.  **Invalid details:** **Start date** 17-04-2027, **Nights** 6, then
    **Search**. The red message "You must be back by 20 April 2027"
    appears.

**Say:** "If my budget is too small, the app shows the cheapest possible
trip and suggests what to change. If no trip is possible, it explains
why. And if I enter invalid details, I get a clear message."

## 10. Closing

**Navigate:** click **Plan a trip** to go back to the home page.

**Say:** "So with Build My Holiday, I search once, pick the package that
suits me, make it my own, get packing tips, and book everything with one
reservation number. Thank you."

## Tips

-   For the Menon search, the **Cheapest** and **Fastest** cards are the
    same trip (the card says "Also the fastest option"). That's
    expected.
-   Run `demo_reset.sql` again after recording, so the booking doesn't
    use up seats for the live demo.
