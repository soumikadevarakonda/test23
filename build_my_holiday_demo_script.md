# Build My Holiday --- Demo Recording Script

## Before you record

1.  **Clear old bookings** so they don't use up seats and rooms:

    ``` bash
    mysql -u holiday -pholiday holiday < database/seeds/demo_reset.sql
    ```

    This deletes **all** saved trips and bookings, including your test
    ones.

2.  **Start the backend:** run `uvicorn app.main:app --reload` in
    `backend/`.

3.  **Start the frontend:** run `npm run dev` in `frontend/`.

4.  **Set up the browser:** open <http://localhost:5173> at 100% zoom,
    full screen, with an empty form.

5.  **Turn off notifications.** Have a notes app open to paste the tips
    list into later (optional).

6.  **Practise the Part A clicks twice.** The numbers below come from
    the real catalog, so they should match on screen.

------------------------------------------------------------------------

## Part A: The Menon family (0:00--4:00)

### 0:00 --- Intro (15 s)

**Show:** the home page.

**Say:**

> Hi, this is Build My Holiday. You search once, and it builds your
> whole holiday --- flights, hotels, transfers and a day-by-day plan ---
> that fits your dates, your group and your budget. Let's plan the Menon
> family's first trip to Japan.

### 0:15 --- Fill the search (35 s)

**Do:** 1. Leaving from: **Bengaluru (BLR)**. Going to: **Japan**. 2.
Start date: **10 Apr 2027**, nights: **6**. 3. Travelers: **2 adults**,
add **1 child**, age **6**. Point at the age picker. 4. Budget:
**₹3,50,000**. 5. **Untick** "Compare 3 options" for now.

**Say:**

> Cities and countries come from the catalog. Children's ages matter for
> fares and room sizes. Under the bar you can see we'd be back on 16
> April. Search.

### 0:50 --- The package (50 s)

**Do:** click **Search**. On the trip page, point at: 1. The top strip:
BLR → Japan, 10--16 Apr, 2 adults + 1 child. 2. **Tokyo 2N → Osaka 4N**.
3. The price summary: **₹2,30,440**, budget **₹3,50,000**, **₹1,19,560
left**.

**Say:**

> The app chose Tokyo for two nights and Osaka for four. Six nights
> gives two cities, with at least two nights in each. Here's the total
> in rupees against the budget, with ₹1.19 lakh left.

**Do:** scroll through Day 1 to Day 3.

**Say:**

> Day by day, in time order. The overnight flight leaves Bengaluru at
> 23:50 on the 9th and lands in Narita on the 10th. Then the airport bus
> to the hotel, check-in, a temple on day 2, and on day 3 the bullet
> train to Osaka. Every package is checked against all the travel rules
> before you see it.

### 1:40 --- Change a flight (35 s)

**Do:** on Day 1, click **Change flight**, point at the price
differences, then choose the later flight (**FL-405**, departing
**06:30**). Point at the green "Your trip was updated" box and the new
total (**₹2,36,180**).

**Say:**

> Every option shows the price difference first. I'll take the morning
> flight.

> Because we now land at 21:30, the airport bus no longer runs. The app
> switched to a taxi at 22:30 by itself, re-checked the whole trip and
> updated the total.

### 2:15 --- Change a hotel and an activity (40 s)

**Do:** 1. On the Osaka stay, click **Change hotel**. Show the search
box and **Sort by guest rating**, then pick another hotel. 2. On a day,
click **Add an activity**, pick one, then **Remove** another. 3. Point
at the version number and the **Undo last change** button.

**Say:**

> Hotels show the rating, stars and room, with search, sort and a
> free-cancellation filter.

> Activities are only offered at times that fit the day and the opening
> hours, so you can't double-book.

> Every change is a new version, and undo is one click.

### 2:55 --- Book it (35 s)

**Do:** click **Book this trip**. Enter a name (e.g. *Rohan Menon*) and
an email, then click **Book now**.

**Say:**

> Book now. Seats and rooms are checked again at this moment, and we get
> one 10-digit booking number for the whole trip.

**Do:** on the confirmation page, click **Copy** next to the booking
number.

### 3:30 --- Open the reservation (30 s)

**Do:** click **Find a booking** in the header, paste the number, and
click **Find booking**. The trip opens. Then type a wrong number,
e.g. `1234567890`.

**Say:**

> Anyone can open the booking by its number. It's stored in MySQL, so it
> still works after a restart.

> And a wrong number shows "Reservation not found".

------------------------------------------------------------------------

## Part B: Extra features (4:00--6:00)

### 4:00 --- Three options (35 s)

**Do:** go to **Plan a trip** and choose the **Dubai & Abu Dhabi**
popular trip (Delhi, 6 nights, ₹3 lakh). Tick **Compare 3 options** and
click **Search**. Point at the three cards: - **Cheapest:** ₹87,264 -
**Fastest:** Dubai only, 435 minutes of travel - **Best rated:** 5-star
hotels, still within budget

Click **Choose** on one, then **← Back to your 3 options**.

**Say:**

> We can also compare three trips: cheapest, fastest and best rated.

### 4:35 --- Budget too small (20 s)

**Do:** search the Menon trip again with budget **₹50,000**.

**Say:**

> When nothing fits the budget, the app says so, shows the cheapest
> possible trip --- ₹2,19,324 --- and suggests what to change.

### 4:55 --- No trip possible, and invalid input (25 s)

**Do:** 1. Search **Chennai → UAE**, 8 Apr, 4 nights, 4 adults and 4
children, ₹6 lakh.

**Say:** "Here no trip is possible, and the app explains why: no return
flight has 8 seats left that day."

2.  Search with start date **18 Apr** and **3 nights**.

    **Say:** "And invalid input gets a clear message: we'd be back after
    20 April."

### 5:20 --- One-line search (15 s)

**Do:** in "Describe your trip in one line", type:

``` text
2 adults 1 kid age 6 Bengaluru to Japan 10 Apr 6 nights 3.5 lakh
```

Then click **Fill search**.

**Say:**

> You can also type the trip in plain words. Rules, not AI, read it and
> fill in the search.

### 5:35 --- Packing tips and city splits (20 s)

**Do:** open any trip and scroll to the bottom.

**Say:**

> At the end there are other ways to split the nights between cities,
> with the price difference, and "Before you go" tips for weather,
> plugs, customs and what to pack for your activities.

### 5:55 --- Close (10 s)

**Say:**

> That's Build My Holiday: one search, a complete trip that stays
> correct as you change it, and one booking number for everything. Thank
> you.

------------------------------------------------------------------------

## Recording tips

-   **Speak slowly.** Pause about a second after each click, so viewers
    see what changed.
-   **Zoom in on numbers:** use the Windows Magnifier (`Win + Plus`) on
    totals and the booking number.
-   **If a click goes wrong,** pause, redo it, and cut the mistake out
    when editing.
-   **To record:** use the Xbox Game Bar (`Win + Alt + R`) or OBS. 1080p
    is enough.
-   **After recording,** run `demo_reset.sql` again so seats and rooms
    are back for the live demo.
