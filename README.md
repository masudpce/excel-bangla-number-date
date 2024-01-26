# excel-bangla-number-date


outline:
1. bangla and indian-bangla language add in windows.


2. bangla number
	after formatting,
	add to the beginning  of the custom-formatting-type
		[$-bn-bn,500]
		or
		[$-bn-in,500]
	
	example:
	[$-bn-bn,500]0
	[$-bn-bn,500]0.0
	[$-bn-bn,500]0.00


3.1 bangla date long format
	after formatting,
	add to the beginning of the custom-formatting-type
		[$-bn-bn,500]
		or
		[$-bn-in,500]
		
	example:
	[$-bn-bn,500]dd-mmm-yyyy          => ১১-ডিসেম্বর-২০২৩ 
	[$-bn-in,500]dd-mmmm-yyyy         => ১১-ডিসেম্বর-২০২৩ 
	
	[$-bn-bn,500]dd/mmm/yyyy          => ১১/ডিসেম্বর/২০২৩ 
	[$-bn-in,500]dd-mmmm-yyyy         => ১১/ডিসেম্বর/২০২৩ 
	
	
3.2 bangla date short-month-name format. like "নভে" 
	after formatting,
	add to the beginning of the custom-formatting-type
		[$-bn-in,500]
	and use this for month 
		mmm
		
	example:
		[$-bn-in,500]dd-mmm-yyyy          => ১১-ডিসে-২০২৩ 
		[$-bn-in,500]dd/mmm/yyyy          => ১১/ডিসে/২০২৩ 
		
		
4. concatenate two bangla date in one cell. 
	The following formula concatenate two dates from cell A1 and A2
	A1 = ১/১/২০২৩                     
	A2 = ২/২ /২০২৫
	
	use "CONCAT" function to join
	use "TEXT" function to format
	
	example:
		=CONCAT(TEXT(A1,"[$-bn-in,500]dd mmm"), " - ", TEXT(A2,"[$-bn-in,500]dd mmm"))
		=>	১ জানু  - ২ ফেব্রু 
	
		=CONCAT(TEXT(A1,"[$-bn-in,500]dd/mmm/yyyy"), " - ", TEXT(A2,"[$-bn-in,500]dd/mmm/yyyy"))
		=>     ১/জানু/২০২৩ - ২/ফেব্রু/২০২৫ 
	
		=CONCAT(TEXT(A1, "[$-bn-in,500]dd/mmm/yyyy"), " থেকে  ", TEXT(A2,"[$-bn-in,500]dd/mmm/yyyy"))
		=>     ১/জানু/২০২৩  থেকে  ২/ফেব্রু/২০২৫ 
