# Buying all the Beer

  ## Premise

  You are tasked with finding you and your friends' favorite beers in PVD's new liquor store.  The store has _n_ different types of beers and each of your _n_ friends favors a different one.  (No two friends have the same favorite beer.)  When you go in the store, it has _n_ aisles with one type of beer stocked in each.  Because you are an alcoholic (duh!), you have to have a taste of every (new) type of beer you see.

  Write a class `BeerSleuth` that has one function `find_alc(beer_type_to_find: str, look_in_aisle: function)` that takes a String of the current favorite beer's name, and a `function look_in_aisle(aisle: int)` that goes to an aisle and buys the beer it holds, otherwise tastes it.


  ## Rules

  - If you taste more than _n/2_ beers (i.e. enter more than _n/2_ aisles) in one shopping session, you black out (the class is reinstantiated).  This is game over.

  - If you go to the aisle containing the current favorite beer, you exit the store, give it to the friend who requested it, and sober up (the class is also reinstantiated).  The current favorite beer will change and you will reenter the store.

  - If you successfully purchace all _n_ favorite beers (1 shopping trip each) without blacking out, you win!


  `BeerSleuth` must have a greater than _30%_ success rate at winning this game (finding and buying all _n_ types of beers) to solve the problem.  The approach of checking aisles randomly only has a _(50%)^n_ success rate.


  ## Sample class template

```python
class BeerSleuth:

	@staticmethod
	def find_alc(beer_type_to_find, look_in_aisle):
		"""
		A naïve approach (shown) is to check each aisle in order.
		This approach has a 0% success rate.
		"""
		k = 0  # aisle number
		while True:
			if look_in_aisle(k) == beer_type_to_find:
				return k
			k = k+1
```

You are not given the list of beer names ahead of time, but they are numeric, so computing `int(beer_type_to_find)` effectively computes a unique integer ID for a beer.  You certainly don't need to hash anything (and _n_ is small-ish).

Again, `beer_type_to_find` is a string containing a beer name, and `look_in_aisle` is a private function that returns the name of the beer brand stocked in the _i_th aisle.

```python
# this is implemented in the autograder only
def look_in_aisle(aisle_i: int) -> string:
	# ...
	return store_inventory[aisle_i]
```






