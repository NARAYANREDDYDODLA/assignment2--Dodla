# assignment2-Dodla
# Narayan Reddy Dodla
## Vikarabad
 Vikarabad is a **town** and mandal in **Vikarabad** district of the Indian state of **Telangana**. It is located in **Vikarabad mandal** of Vikarabad revenue division.

 *****
 ## Travel Experience
 1. Distance from Hyderabad to Missouri is 8473.6 miles.
    1. Packed all my things and headed towards Rajiv Gandhi International Airport which is located at Hyderabad.
    2. It's a total of 25 hours from Hyderabad to Kansas.

2. I have booked United Airlines to travel.
    1. I have taken Air India airlines from Hyderabad to Delhi and connecting flight from Delhi to Kansas via Chicago in United Airlines.
    2. layover is around 2 hours in Chicago Airport.
3. Things which i felt important during travelling
    1. documents which are required.

*****   
* I ate different kind of dishes during travel.
* I have kept my cabin bag with me.
* I have carried my headphones during travel.

Take me to [AboutMe](AboutMe.md)

---
## Beverage Section
This is the beverage, location and price table

| Drink		                     | Location	    | Price    |
| -------------                  | -------------| -------- |
| Wild Strawberry Lemonade Freez | taco bell	| $2.50    |
| Mountain Dew Baja Blast	     | taco bell	| $2.70    |
| Fountain Drink.	             | taco bell    | $1.70    |
| Diet Pepsi	                 | taco bell	| $1.40    |

---
## Pithy Quotes

As **Stephen William Hawking** said:

>Science is not only a disciple of reason but, also, one of romance and passion.

>Intelligence is the ability to adapt to change.


---
## Code Fencing

Inclusion-Exclusion Principle from **Combinatorics**

>Combinatorics is an area of mathematics primarily concerned with counting, both as a means and an end in obtaining results, and certain properties of finite structures.
>It is closely related to many other areas of mathematics and has many applications ranging from logic to statistical physics, from evolutionary biology to computer science, etc.

Inclusion-Exclusion Principle [Reference_link](https://en.wikipedia.org/wiki/Combinatorics)

code for Inclusion-Exclusion Principle

```

int solve (int n, int r) {
    vector<int> p;
    for (int i=2; i*i<=n; ++i)
        if (n % i == 0) {
            p.push_back (i);
            while (n % i == 0)
                n /= i;
        }
    if (n > 1)
        p.push_back (n);

    int sum = 0;
    for (int msk=1; msk<(1<<p.size()); ++msk) {
        int mult = 1,
            bits = 0;
        for (int i=0; i<(int)p.size(); ++i)
            if (msk & (1<<i)) {
                ++bits;
                mult *= p[i];
            }

        int cur = r / mult;
        if (bits % 2 == 1)
            sum += cur;
        else
            sum -= cur;
    }

    return r - sum;
}
```
Inclusion-Exclusion Principle[code_link](https://cp-algorithms.com/combinatorics/inclusion-exclusion.html)










