# nyt_scraping_project
 
## (a) What I wanted to get by scraping.

I wanted to get the following data about the New York Times best sellers for the past 52 weeks: title, author, current rank in the specified week, the date/week, and how many weeks the book has been on the list overall. 

## (b) The steps I took.

I created a function that takes two arguments: the partial url of the week you'd like to start at and how many weeks, n, back you want to go. The function opens the .csv file to prepare to write in it. 
`def get_nyt(url, n):`


Inside the get_nyt function is a for-loop that iterates (n) times. This outer for-loop parses the page for all of the book details as well as the url for the previous week. 
	`for i in range(n):`

The nested for-loop adds each detail (title, author, rank, etc) into its own list that gets written into a row in the csv. The previous link partial url gets reassigned to be the new url and it continues that loop for n times. 
		`for i in range(len(get_books)):`


## (c) Unexpected problems and solutions.

I thought I would need to create a list of URLs to pass through the main function that scrapes each page, but I ended up being able to combine it so that it did everything in one function. The rank of the books were also not explicitly coded in the HTML, so I had to use the index of the books when looping through the code to retrieve the rank.
