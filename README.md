# jump_spot
Calculator for ideal skydive spot based on winds aloft forecast and jump/depoloyment altitude.

Basic overview:
1) look up current id for winds aloft data (api.weather.gov/products?wmoid=FBUS31&type=FD1) - returns list of products

2) get winds aloft data (curl -X GET "https://api.weather.gov/products/{productID})

3) User gives drop airport (or nearest with METAR) and LZ coords

4) locate nearest airport w/ winds aloft data (great circle dist formula)

5) use algorithm to find exit point

6) convert to dist and offset from LZ; find jump run based on winds aloft
