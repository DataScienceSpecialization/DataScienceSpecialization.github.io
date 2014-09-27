I feel the urge to write a sample codebook (for David's FAQ).

It's very similar to a Statistical Analysis Plan, actually.

Setup, there is a dogwalking business. It wants to analyze its work.

Raw data is: name of dog, address of owner, time walked, date walked, size of dog (small, medium, or large), health of dog (well or sick) on that date and time, comments, and pay.

The business wants to assign ID# to the dogs, and codewords to the address to make this data anonymous. There isn't anything to do to the comments--since free text is all over the place.

Codebook:
The dog's name was transformed into an IDNumber (unique) (1-50), 
the address was transformed into a factor, OwnerName (levels Alice, Bob, Charlie, Deborah, Ernest and Fred), 
time and date walked were counted to make WalksPerWeek1, WalksPerWeek2, and WalksPerWeek3. Week1 begins at 00:01UTC on July1, 2014, Week2 begins at 00:01UTC on July8, 2014, Week3 begins at 00:01UTC on July15, 2014. 
Health was summarized as HealthWeek1, HealthWeek2, and HealthWeek3. It is a factor with two levels, Well and Sick. If the dog was sick at any walk during that week, dog was marked sick, else dog was marked well. 
Dog Size was converted into a factor: Large, Medium and Small are the levels.
Comments are dropped. 
Pay is transformed into PayWeek1, PayWeek2, PayWeek3, which is a factor that has two levels (Yes, and No) for correct pay paid during that week.
