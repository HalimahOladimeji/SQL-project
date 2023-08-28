Answer the following questions and provide the SQL queries used to find the answer. 

    
**Question 1: Which cities and countries have the highest level of transaction revenues on the site?**


SQL Queries:
SELECT country, SUM(product_revenue) AS total_revenue
FROM all_sessions
GROUP BY country
ORDER BY total_revenue DESC
LIMIT 10;

SELECT city, SUM(product_revenue) AS total_revenue
FROM all_sessions
GROUP BY city
ORDER BY total_revenue DESC
LIMIT 10;


Answer:
Countries
"United States"	126685611.15
"United Kingdom"	6287589.81
"Canada"	4125152.05
"India"	3382935.13
"Italy"	2127158.02
"Germany"	1748870.81
"Australia"	1400953.26
"Mexico"	1213663.19
"Japan"	1146560.30
"Spain"	1051755.36

Cities
"Mountain View"	29929838.55
"San Francisco"	8312905.21
"Sunnyvale"	8310431.86
"Palo Alto"	7422479.88
"New York"	7155823.47
"San Jose"	3834088.90
"London"	3183845.38
"Chicago"	2879320.27
"Seattle"	2670826.50
"Santa Clara"	2469951.35

**Question 2: What is the average number of products ordered from visitors in each city and country?**


SQL Queries:
SELECT city, country, AVG(product_quantity) AS average_product_quantity
FROM all_sessions
GROUP BY city, country;


Answer:
"San Francisco"	"France"	499.0000000000000000
"Kharagpur"	"India"	46.0000000000000000
"(not set)"	"San Marino"	757.0000000000000000
"Not given"	"Poland"	368.1162790697674419
"Not given"	"Moldova"	1893.0000000000000000
"Stanford"	"United States"	178.0000000000000000
"Not given"	"Ecuador"	136.7272727272727273
"Not given"	"Lithuania"	511.3571428571428571
"Not given"	"Not given"	0.00000000000000000000
"Not given"	"Costa Rica"	573.4000000000000000
"Mexico City"	"Mexico"	723.3750000000000000
"Not given"	"Australia"	550.4927536231884058
"Hayward"	"United States"	137.0000000000000000
"Not given"	"Indonesia"	535.0185185185185185
"Poznan"	"Poland"	73.5000000000000000
"San Salvador"	"El Salvador"	49.0000000000000000
"Coventry"	"United Kingdom"	22.0000000000000000
"Rome"	"Italy"	1310.4000000000000000
"Berkeley"	"United States"	25.0000000000000000
"Colombo"	"Sri Lanka"	138.6666666666666667
"Goose Creek"	"United States"	168.0000000000000000
"Egham"	"United Kingdom"	50.0000000000000000
"Not given"	"Nigeria"	280.1428571428571429
"Prague"	"Czechia"	1216.5000000000000000
"Not given"	"Ethiopia"	1239.0000000000000000
"Doha"	"Qatar"	62.0000000000000000
"Longtan District"	"Taiwan"	845.0000000000000000
"San Bruno"	"United States"	1106.4285714285714286
"Not given"	"Uganda"	1033.0000000000000000
"Not given"	"Myanmar (Burma)"	543.6666666666666667
"Mexico City"	"United States"	160.0000000000000000
"Monterrey"	"Mexico"	393.0000000000000000
"Not given"	"Sweden"	366.7446808510638298
"Cupertino"	"United States"	466.7000000000000000
"(not set)"	"Serbia"	513.5000000000000000
"Los Angeles"	"United States"	401.2222222222222222
"Not given"	"Somalia"	50.0000000000000000
"Not given"	"Hong Kong"	1555.0000000000000000
"(not set)"	"Latvia"	935.0000000000000000
"Not given"	"Germany"	466.5807692307692308
"Not given"	"Oman"	1330.0000000000000000
"Washington"	"United States"	191.1111111111111111
"Stockholm"	"Sweden"	163.4666666666666667
"Bangkok"	"Thailand"	610.3461538461538462
"Kalamazoo"	"United States"	403.0000000000000000
"Greer"	"United States"	26.0000000000000000
"(not set)"	"United Kingdom"	87.6666666666666667
"Boston"	"United States"	313.3157894736842105
"Dublin"	"Ireland"	657.4000000000000000
"Santa Fe"	"Argentina"	1932.5000000000000000
"Not given"	"Bulgaria"	1231.7272727272727273
"Santiago"	"Chile"	3607.0000000000000000
"(not set)"	"United States"	363.9000000000000000
"Sacramento"	"United States"	299.0000000000000000
"Bogota"	"Colombia"	488.0000000000000000
"Not given"	"Luxembourg"	12.0000000000000000
"(not set)"	"Iceland"	0.00000000000000000000
"Not given"	"Peru"	743.8181818181818182
"Detroit"	"United States"	2748.0000000000000000
"Not given"	"Ireland"	354.3793103448275862
"(not set)"	"Singapore"	395.1153846153846154
"Milpitas"	"United States"	66.3750000000000000
"Sao Paulo"	"Brazil"	826.6785714285714286
"Eau Claire"	"United States"	59.6363636363636364
"Richardson"	"United States"	185.0000000000000000
"(not set)"	"Réunion"	2538.0000000000000000
"Izmir"	"Turkey"	58.0000000000000000
"Sakai"	"Japan"	1148.0000000000000000
"Bellflower"	"United States"	3786.0000000000000000
"Riyadh"	"Saudi Arabia"	1138.0000000000000000
"Bratislava"	"Slovakia"	0.00000000000000000000
"Amsterdam"	"United States"	8.0000000000000000
"Not given"	"Belarus"	231.0000000000000000
"Not given"	"Macau"	701.6666666666666667
"Not given"	"Maldives"	33.0000000000000000
"(not set)"	"Netherlands"	
"Nanded"	"India"	53.0000000000000000
"Kharkiv"	"Ukraine"	51.0000000000000000
"Wroclaw"	"Poland"	
"(not set)"	"Kosovo"	433.0000000000000000
"Frankfurt"	"Germany"	65.0000000000000000
"Moscow"	"Russia"	1291.8000000000000000
"Cork"	"Ireland"	3786.0000000000000000
"Not given"	"Papua New Guinea"	2558.0000000000000000
"Jersey City"	"United States"	18.3333333333333333
"Not given"	"Latvia"	309.4285714285714286
"Singapore"	"Singapore"	667.1891891891891892
"Neipu Township"	"Taiwan"	58.0000000000000000
"Melbourne"	"Australia"	659.3750000000000000
"Not given"	"Martinique"	138.5000000000000000
"Fortaleza"	"Brazil"	22.0000000000000000
"Patna"	"India"	327.0000000000000000
"LaFayette"	"United States"	15.0000000000000000
"Wrexham"	"United Kingdom"	1033.0000000000000000
"Zurich"	"Switzerland"	399.6666666666666667
"Las Vegas"	"United States"	26.6666666666666667
"Ann Arbor"	"United States"	290.5609756097560976
"Nashville"	"United States"	1886.0000000000000000
"Mountain View"	"Australia"	33.0000000000000000
"Portland"	"United States"	15.0000000000000000
"Not given"	"Switzerland"	396.6000000000000000
"Hong Kong"	"Hong Kong"	568.8750000000000000
"Bhubaneswar"	"India"	499.0000000000000000
"Not given"	"Czechia"	605.4428571428571429
"Vladivostok"	"Russia"	551.0000000000000000
"Nice"	"France"	
"Panama City"	"United States"	0.00000000000000000000
"Waterloo"	"Canada"	8.0000000000000000
"Charlottetown"	"Canada"	
"Not given"	"Kazakhstan"	617.0000000000000000
"Bucharest"	"Romania"	697.4444444444444444
"Quezon City"	"Philippines"	66.8333333333333333
"La Victoria"	"Peru"	465.2500000000000000
"(not set)"	"Sudan"	
"Not given"	"Gibraltar"	79.0000000000000000
"Singapore"	"France"	433.0000000000000000
"Salford"	"United Kingdom"	171.0000000000000000
"Dubai"	"United Arab Emirates"	798.1428571428571429
"Calgary"	"Canada"	472.2000000000000000
"Not given"	"Nicaragua"	268.0000000000000000
"Not given"	"Japan"	509.2620689655172414
"Chicago"	"United States"	647.2916666666666667
"Not given"	"Sri Lanka"	427.5454545454545455
"Not given"	"Botswana"	215.0000000000000000
"Wellesley"	"United States"	269.0000000000000000
"Mississauga"	"Canada"	1305.2500000000000000
"(not set)"	"Brazil"	433.0000000000000000
"South El Monte"	"United States"	137.0000000000000000
"Not given"	"Ghana"	197.0000000000000000
"Montreal"	"Canada"	313.8947368421052632
"Bandung"	"Indonesia"	53.0000000000000000
"Not given"	"Laos"	886.6666666666666667
"Not given"	"El Salvador"	14.0000000000000000
"Not given"	"Israel"	783.1666666666666667
"Not given"	"India"	421.5954198473282443
"Not given"	"Sudan"	935.0000000000000000
"Chennai"	"India"	497.1969696969696970
"Not given"	"Romania"	847.1562500000000000
"Rio de Janeiro"	"Brazil"	179.6666666666666667
"Not given"	"Mexico"	550.7118644067796610
"Not given"	"Lebanon"	935.0000000000000000
"Not given"	"Thailand"	508.6315789473684211
"(not set)"	"Sint Maarten"	1100.0000000000000000
"(not set)"	"Japan"	93.2500000000000000
"Madison"	"United States"	92.0000000000000000
"Appleton"	"United States"	66.0000000000000000
"Jacksonville"	"United States"	326.5000000000000000
"(not set)"	"Panama"	2.0000000000000000
"Not given"	"Italy"	697.8857142857142857
"Not given"	"Zimbabwe"	844.0000000000000000
"(not set)"	"Switzerland"	1100.0000000000000000
"Not given"	"Taiwan"	409.2666666666666667
"Istanbul"	"Hungary"	363.0000000000000000
"Shinjuku"	"Japan"	565.2857142857142857
"Not given"	"Saudi Arabia"	277.3333333333333333
"Chico"	"United States"	22.0000000000000000
"Helsinki"	"Finland"	31.0000000000000000
"Not given"	"Norway"	397.4827586206896552
"Taguig"	"Philippines"	355.4285714285714286
"New York"	"United States"	431.9614678899082569
"Not given"	"Cyprus"	78.2500000000000000
"Nairobi"	"Kenya"	6.0000000000000000
"Norfolk"	"United States"	102.0000000000000000
"Not given"	"Vietnam"	538.0000000000000000
"Not given"	"Mauritius"	104.5000000000000000
"Not given"	"Slovakia"	525.1428571428571429
"Not given"	"Malta"	469.5000000000000000
"Seattle"	"United States"	478.0280373831775701
"Timisoara"	"Romania"	344.0000000000000000
"Mumbai"	"India"	470.3061224489795918
"Adelaide"	"Australia"	54.0000000000000000
"Brussels"	"Belgium"	62.0000000000000000
"Chiyoda"	"Japan"	0.00000000000000000000
"Not given"	"Brunei"	45.5000000000000000
"Dallas"	"United States"	503.2758620689655172
"Barcelona"	"Spain"	241.5294117647058824
"Oakland"	"United States"	445.4285714285714286
"(not set)"	"Not given"	551.2352941176470588
"Not given"	"Netherlands"	448.8846153846153846
"Budapest"	"Hungary"	184.1666666666666667
"Avon"	"United States"	330.5000000000000000
"Marlboro"	"United States"	0.00000000000000000000
"Johnson City"	"United States"	
"Not given"	"Singapore"	364.8571428571428571
"Pittsburgh"	"United States"	533.7272727272727273
"Not given"	"Croatia"	516.5384615384615385
"Not given"	"Slovenia"	553.8750000000000000
"Quimper"	"France"	
"Esbjerg"	"Denmark"	
"Pune"	"India"	386.5555555555555556
"Not given"	"Canada"	489.8015665796344648
"Warsaw"	"Poland"	463.5217391304347826
"Forest Park"	"United States"	5.0000000000000000
"Thessaloniki"	"Greece"	171.5000000000000000
"London"	"United Kingdom"	501.2093023255813953
"San Francisco"	"Japan"	65.0000000000000000
"Bordeaux"	"France"	0.00000000000000000000
"St. Louis"	"United States"	13.5000000000000000
"Not given"	"Argentina"	344.8333333333333333
"Dublin"	"Netherlands"	844.0000000000000000
"Athens"	"Greece"	1088.4000000000000000
"Ashburn"	"United States"	187.5000000000000000
"Kitchener"	"Canada"	321.4000000000000000
"Phoenix"	"United States"	694.8333333333333333
"Istanbul"	"Turkey"	420.6818181818181818
"Burnaby"	"Canada"	200.6666666666666667
"Saint Petersburg"	"Russia"	1106.7500000000000000
"(not set)"	"Bangladesh"	272.9285714285714286
"Ottawa"	"Canada"	25.5000000000000000
"Antalya"	"Turkey"	0.00000000000000000000
"Watford"	"United Kingdom"	0.00000000000000000000
"Not given"	"Iraq"	150.6666666666666667
"Mountain View"	"Japan"	151.0000000000000000
"Vilnius"	"Lithuania"	40.0000000000000000
"Not given"	"China"	229.0000000000000000
"Not given"	"Montenegro"	3786.0000000000000000
"Not given"	"Armenia"	1351.0000000000000000
"Not given"	"Mali"	3786.0000000000000000
"New York"	"Canada"	178.0000000000000000
"Brno"	"Czechia"	1548.0000000000000000
"Not given"	"Macedonia (FYROM)"	505.0000000000000000
"Sherbrooke"	"Canada"	812.6666666666666667
"Not given"	"Portugal"	1265.9000000000000000
"Vancouver"	"United States"	0.00000000000000000000
"Not given"	"Jersey"	59.0000000000000000
"Austin"	"United States"	570.6914893617021277
"Munich"	"Germany"	865.2857142857142857
"Columbia"	"United States"	154.0000000000000000
"Pozuelo de Alarcon"	"Spain"	541.3333333333333333
"Salem"	"United States"	446.2750000000000000
"Mountain View"	"United States"	576.0410821643286573
"(not set)"	"Canada"	183.0000000000000000
"Oxford"	"United Kingdom"	183.0000000000000000
"Brisbane"	"Australia"	274.5000000000000000
"Oviedo"	"United States"	260.0000000000000000
"Antwerp"	"Belgium"	134.5000000000000000
"Council Bluffs"	"United States"	7589.0000000000000000
"Denver"	"United States"	355.8333333333333333
"Buenos Aires"	"Argentina"	434.5000000000000000
"San Diego"	"United States"	1093.5238095238095238
"Asuncion"	"Paraguay"	15.0000000000000000
"Westlake Village"	"United States"	0.00000000000000000000
"Culiacan"	"Mexico"	220.0000000000000000
"(not set)"	"Bahamas"	917.0000000000000000
"Glasgow"	"United Kingdom"	183.0000000000000000
"Copenhagen"	"Denmark"	61.5000000000000000
"Santa Monica"	"United States"	276.0000000000000000
"Ipoh"	"Malaysia"	362.0000000000000000
"Not given"	"Qatar"	31.0000000000000000
"St. John's"	"Canada"	34.0000000000000000
"Druid Hills"	"United States"	269.0000000000000000
"Charlotte"	"United States"	749.1333333333333333
"Not given"	"Tanzania"	1429.0000000000000000
"Toronto"	"Canada"	570.4678899082568807
"Not given"	"Bolivia"	90.0000000000000000
"Skopje"	"Macedonia (FYROM)"	
"Not given"	"Bahrain"	226.3333333333333333
"Not given"	"Panama"	630.5714285714285714
"Amsterdam"	"Netherlands"	390.4000000000000000
"Lucknow"	"India"	33.0000000000000000
"Jaipur"	"India"	339.5000000000000000
"Not given"	"Kuwait"	221.1666666666666667
"Rexburg"	"United States"	308.6666666666666667
"Hanoi"	"Vietnam"	347.0000000000000000
"Marseille"	"France"	31.0000000000000000
"Not given"	"Albania"	510.3333333333333333
"Belgrade"	"Serbia"	
"Parsippany-Troy Hills"	"United States"	18.0000000000000000
"Tel Aviv-Yafo"	"Israel"	547.7567567567567568
"(not set)"	"Hong Kong"	482.4375000000000000
"Stuttgart"	"Germany"	214.0000000000000000
"Not given"	"Turkey"	350.2424242424242424
"Villeneuve-d'Ascq"	"France"	230.0000000000000000
"San Jose"	"United States"	468.2216981132075472
"Beijing"	"China"	16.0000000000000000
"San Mateo"	"United States"	36.0000000000000000
"Not given"	"Russia"	506.9850746268656716
"Kuala Lumpur"	"Malaysia"	384.5000000000000000
"Auckland"	"New Zealand"	52.0000000000000000
"El Paso"	"United States"	2.0000000000000000
"Fort Worth"	"United States"	0.00000000000000000000
"The Dalles"	"United States"	516.5000000000000000
"Petaling Jaya"	"Malaysia"	53.5000000000000000
"(not set)"	"Dominican Republic"	3.0000000000000000
"Minneapolis"	"United States"	70.0000000000000000
"Oslo"	"Norway"	40.0000000000000000
"University Park"	"United States"	215.0000000000000000
"Not given"	"Serbia"	618.3636363636363636
"Not given"	"Belgium"	237.0178571428571429
"Not given"	"Estonia"	151.2000000000000000
"Redmond"	"United States"	661.1250000000000000
"Not given"	"Algeria"	720.5000000000000000
"Tempe"	"United States"	447.2500000000000000
"Krakow"	"Poland"	
"Philadelphia"	"United States"	315.0000000000000000
"Not given"	"Kenya"	27.0000000000000000
"Not given"	"Morocco"	1203.4285714285714286
"Irvine"	"United States"	379.8888888888888889
"Hyderabad"	"India"	602.3269230769230769
"Not given"	"Egypt"	322.4545454545454545
"Sydney"	"Australia"	396.0909090909090909
"Iasi"	"Romania"	79.0000000000000000
"Quebec City"	"Canada"	578.1428571428571429
"Bengaluru"	"India"	456.4242424242424242
"Bellingham"	"United States"	2836.0000000000000000
"Houston"	"United States"	380.2500000000000000
"Bilbao"	"Spain"	13.5000000000000000
"Kovrov"	"Russia"	58.0000000000000000
"Indore"	"India"	689.0000000000000000
"Madrid"	"Spain"	1286.4666666666666667
"Kirkland"	"United States"	847.7179487179487179
"San Antonio"	"United States"	368.8571428571428571
"Shibuya"	"Japan"	152.0000000000000000
"Amã"	"Jordan"	
"Kolkata"	"India"	593.2222222222222222
"(not set)"	"Peru"	347.1428571428571429
"Boulder"	"United States"	361.0000000000000000
"Hong Kong"	"United States"	363.0000000000000000
"Not given"	"Malaysia"	416.8709677419354839
"(not set)"	"Sri Lanka"	3.0000000000000000
"Milan"	"Italy"	1091.5454545454545455
"Manila"	"Philippines"	128.7500000000000000
"Not given"	"Honduras"	680.5000000000000000
"Not given"	"South Africa"	203.5909090909090909
"(not set)"	"Philippines"	1351.0000000000000000
"Not given"	"Tunisia"	748.0000000000000000
"Perth"	"Australia"	1035.8000000000000000
"Ahmedabad"	"India"	364.6363636363636364
"Sandton"	"South Africa"	183.0000000000000000
"Jakarta"	"Indonesia"	347.7826086956521739
"Vienna"	"Austria"	228.5000000000000000
"Not given"	"Spain"	417.6818181818181818
"Makati"	"Philippines"	51.5000000000000000
"Alexandria"	"Egypt"	
"Tampa"	"United States"	168.0000000000000000
"Zhongli District"	"Taiwan"	1492.0000000000000000
"Not given"	"Chile"	261.8000000000000000
"Fremont"	"United States"	401.5000000000000000
"Rosario"	"Argentina"	433.0000000000000000
"Sunnyvale"	"United States"	491.9389067524115756
"Montreuil"	"France"	726.5000000000000000
"Sapporo"	"Japan"	12.0000000000000000
"Not given"	"Jordan"	295.0000000000000000
"Rotterdam"	"Netherlands"	0.00000000000000000000
"(not set)"	"Taiwan"	842.6055045871559633
"Not given"	"France"	447.2357142857142857
"Not given"	"Colombia"	411.7931034482758621
"Palo Alto"	"United States"	703.4367816091954023
"Karachi"	"Pakistan"	428.0000000000000000
"Courbevoie"	"France"	348.0000000000000000
"Not given"	"Côte d’Ivoire"	1309.3333333333333333
"(not set)"	"India"	691.2058823529411765
"Chandigarh"	"India"	15.0000000000000000
"Not given"	"South Korea"	486.7391304347826087
"Not given"	"Bosnia & Herzegovina"	6.0000000000000000
"Raleigh"	"United States"	
"Not given"	"Cambodia"	362.2000000000000000
"Not given"	"Philippines"	547.0923076923076923
"Not given"	"French Polynesia"	
"San Francisco"	"United States"	503.7333333333333333
"Yokohama"	"Japan"	91.8333333333333333
"Kansas City"	"United States"	4.0000000000000000
"Nagoya"	"Japan"	22.0000000000000000
"(not set)"	"Nepal"	212.0000000000000000
"Chuo"	"Japan"	65.0000000000000000
"Kiev"	"Ukraine"	400.5625000000000000
"Gothenburg"	"Sweden"	
"Not given"	"Dominican Republic"	912.2000000000000000
"Not given"	"Iceland"	
"Zagreb"	"Croatia"	54.0000000000000000
"Not given"	"Guatemala"	603.2222222222222222
"Akron"	"United States"	15.0000000000000000
"Cape Town"	"South Africa"	25.0000000000000000
"Edmonton"	"Canada"	569.5000000000000000
"East Lansing"	"United States"	66.0000000000000000
"(not set)"	"Belize"	
"Lake Oswego"	"United States"	215.0000000000000000
"Belo Horizonte"	"Brazil"	1184.0000000000000000
"Bangkok"	"United States"	7.0000000000000000
"Not given"	"Georgia"	2506.4000000000000000
"Not given"	"New Zealand"	464.2272727272727273
"Vancouver"	"Canada"	395.0000000000000000
"Montevideo"	"Uruguay"	292.5000000000000000
"(not set)"	"Puerto Rico"	3.0000000000000000
"Lahore"	"Pakistan"	218.0000000000000000
"Not given"	"Denmark"	598.7037037037037037
"(not set)"	"Thailand"	73.0000000000000000
"Not given"	"Greece"	443.4642857142857143
"Not given"	"Finland"	337.3333333333333333
"Paris"	"United States"	6.0000000000000000
"Odessa"	"Ukraine"	
"Not given"	"United Kingdom"	610.0225563909774436
"Piscataway Township"	"United States"	40.0000000000000000
"(not set)"	"Indonesia"	1360.0000000000000000
"Not given"	"Jamaica"	178.0000000000000000
"(not set)"	"Côte d’Ivoire"	3786.0000000000000000
"(not set)"	"Palestine"	155.0000000000000000
"Not given"	"Kyrgyzstan"	123.0000000000000000
"New Delhi"	"India"	487.6944444444444444
"Not given"	"Venezuela"	359.0000000000000000
"Medellin"	"Colombia"	208.0000000000000000
"Not given"	"Pakistan"	539.7179487179487179
"Not given"	"Puerto Rico"	1319.2000000000000000
"Osaka"	"Japan"	434.3333333333333333
"Berlin"	"Germany"	708.7692307692307692
"Santa Clara"	"United States"	826.8275862068965517
"Columbus"	"United States"	8.5000000000000000
"Manchester"	"United Kingdom"	50.5000000000000000
"Cambridge"	"United States"	627.1250000000000000
"Not given"	"Uruguay"	384.3333333333333333
"Paris"	"France"	352.8837209302325581
"(not set)"	"Bosnia & Herzegovina"	1148.0000000000000000
"Westville"	"South Africa"	2299.0000000000000000
"Orlando"	"United States"	100.1666666666666667
"Ho Chi Minh City"	"Vietnam"	378.3333333333333333
"(not set)"	"Greece"	114.1428571428571429
"Atlanta"	"United States"	474.8275862068965517
"Los Angeles"	"Australia"	917.0000000000000000
"Toronto"	"United States"	168.0000000000000000
"Not given"	"Hungary"	383.4285714285714286
"Not given"	"Haiti"	1.00000000000000000000
"Not given"	"Barbados"	25.0000000000000000
"Not given"	"United States"	506.1102253985706432
"Yokohama"	"United States"	25.0000000000000000
"Not given"	"Austria"	331.5862068965517241
"Redwood City"	"United States"	435.1666666666666667
"Seoul"	"South Korea"	670.5454545454545455
"Not given"	"Bangladesh"	217.8823529411764706
"Maracaibo"	"Venezuela"	119.5000000000000000
"Hamburg"	"Germany"	437.0909090909090909
"Not given"	"Rwanda"	0.00000000000000000000
"Not given"	"Ukraine"	587.5142857142857143
"Pleasanton"	"United States"	330.0000000000000000
"Menlo Park"	"United States"	791.0000000000000000
"Not given"	"Nepal"	746.0000000000000000
"South San Francisco"	"United States"	159.5000000000000000
"Cluj-Napoca"	"Romania"	62.0000000000000000
"Not given"	"United Arab Emirates"	316.2000000000000000
"Not given"	"Brazil"	538.1702127659574468
"Minato"	"Japan"	1033.6969696969696970
"Lisbon"	"Portugal"	299.0000000000000000
"Indianapolis"	"United States"	769.0000000000000000
"London"	"United States"	10.6666666666666667
"Not given"	"Bahamas"	79.0000000000000000
"(not set)"	"Trinidad & Tobago"	1379.5000000000000000
"Ghent"	"Belgium"	1351.0000000000000000
"Gurgaon"	"India"	1335.8571428571428571




**Question 3: Is there any pattern in the types (product categories) of products ordered from visitors in each city and country?**


SQL Queries:
SELECT city, country, v2_product_category
FROM all_sessions    
GROUP BY city, country, v2_product_category;

SELECT city, country, v2_product_category, COUNT(*) AS order_numbers
FROM all_sessions    
GROUP BY city, country, v2_product_category
ORDER BY order_numbers DESC;


Answer:
The highest product category ordered from the United States, United Kingdom, Germany, Canada, India, France, Netherlands, Italy and almost all other countries is "Home/Shop by Brand/YouTube/".


**Question 4: What is the top-selling product from each city/country? Can we find any pattern worthy of noting in the products sold?**


SQL Queries:
SELECT city, country, v2_product_name, SUM(product_quantity) AS total_quantity
FROM all_sessions   
GROUP BY city, country, v2_product_name
HAVING SUM(product_quantity) = (
    	SELECT MAX(total_quantity)
    FROM (
        SELECT city, country, v2_product_name, SUM(product_quantity) AS total_quantity
        FROM all_sessions   
        GROUP BY city, country, v2_product_name
    ) AS subquery
    WHERE subquery.city = all_sessions.city AND subquery.country = all_sessions.country
);


Answer:
"Budapest"	"Hungary"	"Recycled Mouse Pad"	1033
"Brisbane"	"Australia"	"YouTube Twill Cap"	1429
"Not given"	"Uganda"	"Google Laptop and Cell Phone Stickers"	1033
"Phoenix"	"United States"	"Nest® Cam Indoor Security Camera - USA"	2139
"(not set)"	"Panama"	"Google Men's Short Sleeve Hero Tee Light Blue"	2
"Seattle"	"United States"	"Nest® Cam Indoor Security Camera - USA"	4278
"Not given"	"Netherlands"	"YouTube Custom Decals"	7572
"Milan"	"Italy"	"SPF-15 Slim & Slender Lip Balm"	3682
"Singapore"	"France"	"Google Men's Vintage Badge Tee Black"	433
"Riyadh"	"Saudi Arabia"	"Leatherette Journal"	3071
"Belo Horizonte"	"Brazil"	"Collapsible Shopping Bag"	1184
"Not given"	"Finland"	"Recycled Mouse Pad"	1033
"Chandigarh"	"India"	"Google Men's 100% Cotton Short Sleeve Hero Tee Navy"	15
"(not set)"	"San Marino"	"22 oz YouTube Bottle Infuser"	1465
"Makati"	"Philippines"	"Google G Noise-reducing Bluetooth Headphones"	101
"(not set)"	"Japan"	"Electronics Accessory Pouch"	330
"Not given"	"Jordan"	"Set of 3 Packing Cubes"	295
"Kovrov"	"Russia"	"Google Women's Fleece Hoodie"	58
"Philadelphia"	"United States"	"Leatherette Journal"	3071
"Nanded"	"India"	"YouTube Men's Short Sleeve Hero Tee Charcoal"	53
"Ghent"	"Belgium"	"Windup Android"	1351
"El Paso"	"United States"	"Google Men's Short Sleeve Hero Tee Light Blue"	2
"Bordeaux"	"France"	"YouTube Luggage Tag"	0
"Edmonton"	"Canada"	"Google Stylus Pen w/ LED Light"	1100
"(not set)"	"Not given"	"YouTube Custom Decals"	3786
"Minneapolis"	"United States"	"Google Men's Vintage Badge Tee White"	137
"Sapporo"	"Japan"	"Android Toddler Short Sleeve T-shirt Pink"	12
"Goose Creek"	"United States"	"Android Wool Heather Cap Heather/Black"	168
"Not given"	"Mali"	"YouTube Custom Decals"	3786
"Not given"	"Armenia"	"Windup Android"	1351
"Sacramento"	"United States"	"Google Blackout Cap"	299
"Not given"	"Luxembourg"	"Google Toddler Raglan Shirt Blue Heather/Navy"	12
"Istanbul"	"Hungary"	"Android Sticker Sheet Ultra Removable"	363
"(not set)"	"India"	"YouTube Custom Decals"	15144
"Piscataway Township"	"United States"	"Google Men's 100% Cotton Short Sleeve Hero Tee Red"	40
"Santa Clara"	"United States"	"Google Kick Ball"	15170
"Sandton"	"South Africa"	"Google Water Resistant Bluetooth Speaker"	183
"London"	"United Kingdom"	"YouTube Twill Cap"	12861
"La Victoria"	"Peru"	"22 oz YouTube Bottle Infuser"	1465
"Warsaw"	"Poland"	"YouTube Custom Decals"	3786
"Paris"	"France"	"YouTube Custom Decals"	3786
"Not given"	"Macau"	"YouTube Leatherette Notebook Combo"	1148
"Not given"	"Lebanon"	"YouTube RFID Journal"	935
"Not given"	"Norway"	"YouTube Custom Decals"	3786
"Chennai"	"India"	"22 oz YouTube Bottle Infuser"	7325
"Maracaibo"	"Venezuela"	"Google Power Bank"	218
"Sakai"	"Japan"	"YouTube Leatherette Notebook Combo"	1148
"Poznan"	"Poland"	"Google Bongo Cupholder Bluetooth Speaker"	85
"Not given"	"Tanzania"	"YouTube Twill Cap"	1429
"Pune"	"India"	"Plastic Sliding Flashlight"	1570
"Not given"	"Sweden"	"YouTube Leatherette Notebook Combo"	3444
"Dallas"	"United States"	"Google Sunglasses"	4204
"Vladivostok"	"Russia"	"Google Canvas Tote Natural/Navy"	551
"Not given"	"Chile"	"YouTube Leatherette Notebook Combo"	1148
"(not set)"	"Bahamas"	"Google Twill Cap"	917
"Not given"	"Cyprus"	"Suitcase Organizer Cubes"	295
"Columbia"	"United States"	"Google Device Stand"	154
"Not given"	"Iraq"	"Google Men's Vintage Badge Tee Black"	433
"Santiago"	"Chile"	"Google Kick Ball"	15170
"Not given"	"Turkey"	"YouTube Hard Cover Journal"	3990
"Bangkok"	"Thailand"	"Google Metallic Notebook Set"	2718
"Not given"	"India"	"YouTube Custom Decals"	34074
"New York"	"Canada"	"Google Men's  Zip Hoodie"	178
"Bengaluru"	"India"	"YouTube Custom Decals"	3786
"Wellesley"	"United States"	"Colored Pencil Set"	269
"Rotterdam"	"Netherlands"	"YouTube Wool Heather Cap Heather/Black"	0
"Hayward"	"United States"	"Google Men's Vintage Badge Tee White"	137
"Medellin"	"Colombia"	"Bottle Opener Clip"	362
"Villeneuve-d'Ascq"	"France"	"Google Snapback Hat Black"	230
"Panama City"	"United States"	"Google Men's Convertible Vest-Jacket Pewter"	0
"Barcelona"	"Spain"	"Google Laptop and Cell Phone Stickers"	1033
"Westville"	"South Africa"	"Sport Bag"	2299
"Not given"	"Bolivia"	"YouTube Men's Short Sleeve Hero Tee Black"	151
"Quebec City"	"Canada"	"YouTube Custom Decals"	3786
"Fremont"	"United States"	"Windup Android"	1351
"Not given"	"Papua New Guinea"	"YouTube Custom Decals"	3786
"Copenhagen"	"Denmark"	"Rocket Flashlight"	123
"Not given"	"Morocco"	"YouTube Custom Decals"	3786
"Oakland"	"United States"	"Google Doodle Decal"	1290
"Paris"	"United States"	"Google Women's Quilted Insulated Vest Black"	6
"(not set)"	"Sint Maarten"	"Google Stylus Pen w/ LED Light"	1100
"Greer"	"United States"	"Google Men's Quilted Insulated Vest Black"	26
"Not given"	"Argentina"	"YouTube Hard Cover Journal"	2660
"Bogota"	"Colombia"	"SPF-15 Slim & Slender Lip Balm"	3682
"Rio de Janeiro"	"Brazil"	"Google Blackout Cap"	299
"Antwerp"	"Belgium"	"Colored Pencil Set"	269
"Atlanta"	"United States"	"YouTube Custom Decals"	7572
"(not set)"	"Philippines"	"Windup Android"	1351
"Ashburn"	"United States"	"Compact Selfie Stick"	268
"Bilbao"	"Spain"	"Google Women's Short Sleeve Hero Tee Sky Blue"	27
"Rexburg"	"United States"	"Google 17oz Stainless Steel Sport Bottle"	716
"Not given"	"Barbados"	"Google Men's Pullover Hoodie Grey"	25
"Cambridge"	"United States"	"Google 22 oz Water Bottle"	8942
"Antalya"	"Turkey"	"Google Tube Power Bank"	0
"Mountain View"	"Japan"	"Google 5-Panel Snapback Cap"	151
"Mexico City"	"United States"	"Google Lunch Bag"	160
"Vilnius"	"Lithuania"	"Google Men's 100% Cotton Short Sleeve Hero Tee Red"	40
"Not given"	"Austria"	"YouTube Custom Decals"	3786
"Not given"	"Australia"	"22 oz YouTube Bottle Infuser"	7325
"Indore"	"India"	"YouTube Hard Cover Journal"	1330
"Tel Aviv-Yafo"	"Israel"	"Google 22 oz Water Bottle"	8942
"Kiev"	"Ukraine"	"Maze Pen"	1748
"Not given"	"Sudan"	"YouTube RFID Journal"	935
"Not given"	"Israel"	"YouTube Custom Decals"	3786
"Hong Kong"	"United States"	"Android Sticker Sheet Ultra Removable"	363
"Vienna"	"Austria"	"Google Men's 100% Cotton Short Sleeve Hero Tee White"	528
"Dubai"	"United Arab Emirates"	"Leatherette Journal"	3071
"Manila"	"Philippines"	"8 pc Android Sticker Sheet"	336
"Austin"	"United States"	"Google 22 oz Water Bottle"	8942
"Not given"	"Guatemala"	"YouTube Twill Cap"	1429
"Boulder"	"United States"	"YouTube Twill Cap"	1429
"Charlotte"	"United States"	"Google 22 oz Water Bottle"	8942
"(not set)"	"Taiwan"	"Google Kick Ball"	15170
"Not given"	"Montenegro"	"YouTube Custom Decals"	3786
"(not set)"	"Peru"	"22 oz YouTube Bottle Infuser"	1465
"Not given"	"Poland"	"YouTube Custom Decals"	3786
"Not given"	"Estonia"	"22 oz Android Bottle"	597
"Hyderabad"	"India"	"YouTube Custom Decals"	7572
"Cork"	"Ireland"	"YouTube Custom Decals"	3786
"Avon"	"United States"	"Bottle Opener Clip"	362
"Not given"	"Myanmar (Burma)"	"22 oz YouTube Bottle Infuser"	1465
"Not given"	"Portugal"	"Google Kick Ball"	15170
"Glasgow"	"United Kingdom"	"Google Water Resistant Bluetooth Speaker"	183
"Not given"	"Romania"	"YouTube Custom Decals"	15144
"Berkeley"	"United States"	"YouTube Onesie Heather"	25
"Ottawa"	"Canada"	"YouTube Men's Short Sleeve Hero Tee White"	50
"Not given"	"Maldives"	"Google Men's Performance Full Zip Jacket Black"	33
"Kolkata"	"India"	"YouTube Custom Decals"	7572
"Not given"	"Martinique"	"Google Water Resistant Bluetooth Speaker"	183
"Timisoara"	"Romania"	"Galaxy Screen Cleaning Cloth"	844
"Appleton"	"United States"	"Aluminum Handy Emergency Flashlight"	66
"New Delhi"	"India"	"YouTube Custom Decals"	7572
"Kuala Lumpur"	"Malaysia"	"Four Color Retractable Pen"	2002
"Coventry"	"United Kingdom"	"YouTube Youth Short Sleeve Tee Red"	22
"Oviedo"	"United States"	"Google Luggage Tag"	629
"(not set)"	"Dominican Republic"	"Google Women's Lightweight Microfleece Jacket"	3
"Not given"	"Jamaica"	"Google Men's  Zip Hoodie"	178
"(not set)"	"Indonesia"	"Google Metallic Notebook Set"	2718
"Forest Park"	"United States"	"Google Men's Microfiber 1/4 Zip Pullover Blue/Indigo"	5
"Not given"	"Georgia"	"YouTube Custom Decals"	11358
"(not set)"	"Bosnia & Herzegovina"	"YouTube Leatherette Notebook Combo"	1148
"Not given"	"Colombia"	"22 oz YouTube Bottle Infuser"	5860
"Not given"	"Honduras"	"Nest® Cam Outdoor Security Camera - USA"	2719
"Lucknow"	"India"	"YouTube Men's Vintage Tank"	63
"Not given"	"Belgium"	"YouTube Leatherette Notebook Combo"	3444
"Montevideo"	"Uruguay"	"Google Men's 100% Cotton Short Sleeve Hero Tee White"	528
"Not given"	"El Salvador"	"Google Women's Short Sleeve V-Neck Tee Lavender"	33
"Not given"	"Nepal"	"22 oz YouTube Bottle Infuser"	1465
"(not set)"	"Iceland"	"Google Insulated Stainless Steel Bottle"	0
"Eau Claire"	"United States"	"Seat Pack Organizer"	160
"Not given"	"Belarus"	"Google Stylus Pen w/ LED Light"	1100
"Amsterdam"	"Netherlands"	"YouTube Hard Cover Journal"	1330
"Jaipur"	"India"	"Google Men's 100% Cotton Short Sleeve Hero Tee White"	528
"Palo Alto"	"United States"	"Nest® Cam Outdoor Security Camera - USA"	19033
"San Jose"	"United States"	"YouTube Custom Decals"	11358
"Bratislava"	"Slovakia"	"Nest® Learning Thermostat 3rd Gen-USA - Copper"	0
"Egham"	"United Kingdom"	"YouTube Men's Short Sleeve Hero Tee White"	50
"Not given"	"Jersey"	"Google Tri-blend Hoodie Grey"	59
"Richardson"	"United States"	"Micro Wireless Earbud"	185
"(not set)"	"Greece"	"20 oz Stainless Steel Insulated Tumbler"	499
"Not given"	"Not given"	"Google Trucker Hat"	0
"Rosario"	"Argentina"	"Google Men's Vintage Badge Tee Black"	433
"Jersey City"	"United States"	"Google Youth Short Sleeve Tee White"	29
"Izmir"	"Turkey"	"Google Women's Short Sleeve Hero Tee Black"	95
"Not given"	"Germany"	"YouTube Custom Decals"	26502
"Orlando"	"United States"	"Suitcase Organizer Cubes"	295
"Not given"	"Tunisia"	"22 oz YouTube Bottle Infuser"	1465
"Kalamazoo"	"United States"	"Satin Black Ballpoint Pen"	403
"Not given"	"Nicaragua"	"Compact Selfie Stick"	268
"Bhubaneswar"	"India"	"20 oz Stainless Steel Insulated Tumbler"	499
"Not given"	"France"	"YouTube Custom Decals"	15144
"Montreuil"	"France"	"Collapsible Shopping Bag"	1184
"Not given"	"Algeria"	"YouTube Twill Cap"	1429
"Waterloo"	"Canada"	"Google Long Sleeve Raglan Badge Henley Ocean Blue"	8
"Lake Oswego"	"United States"	"Recycled Mouse Pad"	1033
"Ann Arbor"	"United States"	"Koozie Can Kooler"	2442
"(not set)"	"Hong Kong"	"YouTube Custom Decals"	3786
"Not given"	"Slovenia"	"22 oz YouTube Bottle Infuser"	1465
"Singapore"	"Singapore"	"Google 22 oz Water Bottle"	8942
"Chiyoda"	"Japan"	"24 oz YouTube Sergeant Stripe Bottle"	0
"Melbourne"	"Australia"	"YouTube Custom Decals"	3786
"(not set)"	"Switzerland"	"Google Stylus Pen w/ LED Light"	1100
"London"	"United States"	"YouTube Onesie Heather"	25
"Brussels"	"Belgium"	"Google Men's 100% Cotton Short Sleeve Hero Tee Black"	62
"Berlin"	"Germany"	"YouTube Custom Decals"	3786
"Pleasanton"	"United States"	"Electronics Accessory Pouch"	330
"Rome"	"Italy"	"Leatherette Journal"	3071
"The Dalles"	"United States"	"Google Laptop and Cell Phone Stickers"	1033
"Nagoya"	"Japan"	"Google Women's Convertible Vest-Jacket Sea Foam Green"	22
"Montreal"	"Canada"	"Four Color Retractable Pen"	2002
"Patna"	"India"	"22 oz Android Bottle"	597
"Marseille"	"France"	"Google Men's 100% Cotton Short Sleeve Hero Tee Black"	62
"Moscow"	"Russia"	"Google Kick Ball"	15170
"Tempe"	"United States"	"Windup Android"	1351
"Irvine"	"United States"	"Nest® Learning Thermostat 3rd Gen-USA - Stainless Steel"	1886
"Not given"	"Brazil"	"YouTube Custom Decals"	11358
"Not given"	"Malta"	"YouTube RFID Journal"	935
"(not set)"	"Sri Lanka"	"Google Men's Skater Tee Grey"	3
"Yokohama"	"United States"	"Google Men's Pullover Hoodie"	25
"Mumbai"	"India"	"YouTube Custom Decals"	7572
"Not given"	"Rwanda"	"YouTube Wool Heather Cap Heather/Black"	0
"Not given"	"Indonesia"	"YouTube Custom Decals"	7572
"Redmond"	"United States"	"YouTube RFID Journal"	1870
"Not given"	"Macedonia (FYROM)"	"22 oz YouTube Bottle Infuser"	1465
"Not given"	"South Korea"	"YouTube Custom Decals"	3786
"Not given"	"Egypt"	"22 oz YouTube Bottle Infuser"	1465
"Not given"	"Botswana"	"Waterproof Backpack"	215
"Karachi"	"Pakistan"	"YouTube RFID Journal"	935
"Chicago"	"United States"	"Google Kick Ball"	30340
"Watford"	"United Kingdom"	"YouTube Luggage Tag"	0
"Salem"	"United States"	"Google Sunglasses"	4204
"Westlake Village"	"United States"	"Google Men's Long Sleeve Raglan Ocean Blue"	0
"Not given"	"Japan"	"YouTube Custom Decals"	11358
"South San Francisco"	"United States"	"Android Sticker Sheet Ultra Removable"	363
"Kitchener"	"Canada"	"Recycled Mouse Pad"	1033
"Amsterdam"	"United States"	"Google Men's Long Sleeve Raglan Ocean Blue"	8
"Not given"	"Cambodia"	"YouTube Twill Cap"	1429
"Not given"	"Thailand"	"YouTube Custom Decals"	3786
"Jacksonville"	"United States"	"20 oz Stainless Steel Insulated Tumbler"	499
"Fort Worth"	"United States"	"YouTube Trucker Hat"	0
"Not given"	"Bangladesh"	"YouTube Leatherette Notebook Combo"	1148
"Not given"	"South Africa"	"YouTube Twill Cap"	1429
"Not given"	"Singapore"	"22 oz YouTube Bottle Infuser"	1465
"Not given"	"Saudi Arabia"	"YouTube Twill Cap"	1429
"Not given"	"Bahrain"	"Google Men's 100% Cotton Short Sleeve Hero Tee White"	528
"San Antonio"	"United States"	"YouTube Twill Cap"	1429
"Chico"	"United States"	"Android Men's Long Sleeve Badge Crew Tee Heather"	44
"Brno"	"Czechia"	"Leatherette Journal"	3071
"Burnaby"	"Canada"	"Google Men's 100% Cotton Short Sleeve Hero Tee White"	528
"Kharkiv"	"Ukraine"	"Google Women's V-Neck Tee Charcoal"	51
"Menlo Park"	"United States"	"Nest® Cam Indoor Security Camera - USA"	2139
"Oslo"	"Norway"	"Google Men's 100% Cotton Short Sleeve Hero Tee Red"	40
"Not given"	"Kenya"	"Google Women's Short Sleeve Hero Tee Grey"	30
"Not given"	"Zimbabwe"	"Galaxy Screen Cleaning Cloth"	844
"Saint Petersburg"	"Russia"	"Leatherette Journal"	3071
"San Francisco"	"United States"	"Google Kick Ball"	30340
"San Francisco"	"Japan"	"Google Women's Scoop Neck Tee Black"	65
"Ipoh"	"Malaysia"	"Bottle Opener Clip"	362
"Istanbul"	"Turkey"	"YouTube Custom Decals"	3786
"Toronto"	"United States"	"Android Wool Heather Cap Heather/Black"	168
"Washington"	"United States"	"22 oz YouTube Bottle Infuser"	1465
"Not given"	"Latvia"	"YouTube Twill Cap"	1429
"Athens"	"Greece"	"Sport Bag"	2299
"(not set)"	"Thailand"	"Android RFID Journal"	73
"University Park"	"United States"	"Waterproof Backpack"	215
"(not set)"	"Singapore"	"SPF-15 Slim & Slender Lip Balm"	3682
"Zhongli District"	"Taiwan"	"Spiral Notebook and Pen Set"	3582
"(not set)"	"Bangladesh"	"22 oz YouTube Bottle Infuser"	1465
"Not given"	"Uruguay"	"22 oz YouTube Bottle Infuser"	1465
"Not given"	"Mexico"	"YouTube Twill Cap"	4287
"Seoul"	"South Korea"	"YouTube Custom Decals"	3786
"Columbus"	"United States"	"Android Men's  Zip Hoodie"	12
"Denver"	"United States"	"Google Twill Cap"	917
"Not given"	"Italy"	"YouTube Custom Decals"	15144
"Not given"	"Ethiopia"	"YouTube Hard Cover Journal"	1330
"Madison"	"United States"	"Google Tote Bag"	92
"(not set)"	"Serbia"	"Android Spiral Journal with Pen"	665
"Not given"	"Finland"	"Google Laptop and Cell Phone Stickers"	1033
"Not given"	"Greece"	"Leatherette Journal"	3071
"Not given"	"China"	"YouTube Twill Cap"	1429
"Sao Paulo"	"Brazil"	"22 oz Mini Mountain Bottle"	8942
"Mountain View"	"Australia"	"Google Men's Performance Full Zip Jacket Black"	33
"Frankfurt"	"Germany"	"Google Bib White"	65
"Not given"	"Dominican Republic"	"YouTube Custom Decals"	3786
"Not given"	"United Arab Emirates"	"22 oz YouTube Bottle Infuser"	1465
"Not given"	"Côte d’Ivoire"	"YouTube Custom Decals"	3786
"Not given"	"Laos"	"YouTube Hard Cover Journal"	2660
"San Francisco"	"France"	"20 oz Stainless Steel Insulated Tumbler"	499
"Osaka"	"Japan"	"Nest® Protect Smoke + CO White Wired Alarm-USA"	1244
"(not set)"	"Puerto Rico"	"Android Men's Short Sleeve Tri-blend Hero Tee Grey"	3
"East Lansing"	"United States"	"25L Classic Rucksack"	66
"Hanoi"	"Vietnam"	"26 oz Double Wall Insulated Bottle"	845
"Not given"	"Brunei"	"YouTube Men's Vintage Henley"	79
"Culiacan"	"Mexico"	"20 oz Stainless Steel Insulated Tumbler"	499
"Petaling Jaya"	"Malaysia"	"Google Women's Short Sleeve Hero Tee Black"	95
"Parsippany-Troy Hills"	"United States"	"Google Men's Lightweight Microfleece Jacket Black"	18
"Indianapolis"	"United States"	"Ballpoint Stylus Pen"	769
"Auckland"	"New Zealand"	"Google G Noise-reducing Bluetooth Headphones"	101
"Lahore"	"Pakistan"	"Google Power Bank"	218
"Not given"	"Croatia"	"YouTube Custom Decals"	3786
"Kirkland"	"United States"	"Google Kick Ball"	15170
"Not given"	"Kazakhstan"	"Collapsible Shopping Bag"	1184
"Las Vegas"	"United States"	"Google Men's 100% Cotton Short Sleeve Hero Tee Black"	62
"Not given"	"New Zealand"	"YouTube Custom Decals"	7572
"Stuttgart"	"Germany"	"Google Pocket Bluetooth Speaker"	214
"Not given"	"Bahamas"	"YouTube Men's Vintage Henley"	79
"(not set)"	"Réunion"	"YouTube Custom Decals"	3786
"(not set)"	"Kosovo"	"Google Men's Vintage Badge Tee Black"	433
"Portland"	"United States"	"YouTube Men's Short Sleeve Hero Tee Charcoal"	53
"Adelaide"	"Australia"	"Google Men's Watershed Full Zip Hoodie Grey"	54
"Toronto"	"Canada"	"YouTube Custom Decals"	7572
"Shinjuku"	"Japan"	"Plastic Sliding Flashlight"	1570
"Monterrey"	"Mexico"	"YouTube Leatherette Notebook Combo"	1148
"Not given"	"Ireland"	"YouTube Custom Decals"	3786
"Dublin"	"Ireland"	"Google Kick Ball"	15170
"Mississauga"	"Canada"	"YouTube Custom Decals"	3786
"Zurich"	"Switzerland"	"Sport Bag"	4598
"Boston"	"United States"	"Collapsible Shopping Bag"	2368
"Mexico City"	"Mexico"	"Google 22 oz Water Bottle"	8942
"Not given"	"Vietnam"	"YouTube Custom Decals"	3786
"San Bruno"	"United States"	"Google Kick Ball"	15170
"Ahmedabad"	"India"	"YouTube Leatherette Notebook Combo"	1148
"San Mateo"	"United States"	"Google Tri-blend Hoodie Grey"	59
"Iasi"	"Romania"	"YouTube Men's Vintage Henley"	79
"Prague"	"Czechia"	"YouTube Custom Decals"	3786
"South El Monte"	"United States"	"Google Men's Vintage Badge Tee White"	137
"Stanford"	"United States"	"Google Men's  Zip Hoodie"	178
"Not given"	"Gibraltar"	"YouTube Men's Eco-Jersey Henley"	79
"Vancouver"	"Canada"	"YouTube Hard Cover Journal"	1330
"Not given"	"Ukraine"	"YouTube Custom Decals"	7572
"Not given"	"Costa Rica"	"Plastic Sliding Flashlight"	1570
"Bellflower"	"United States"	"YouTube Custom Decals"	7572
"Not given"	"Mauritius"	"Google Power Bank"	156
"Chuo"	"Japan"	"Google Women's Scoop Neck Tee Black"	65
"(not set)"	"Côte d’Ivoire"	"YouTube Custom Decals"	3786
"Not given"	"Malaysia"	"Four Color Retractable Pen"	2002
"Santa Fe"	"Argentina"	"SPF-15 Slim & Slender Lip Balm"	3682
"Norfolk"	"United States"	"Suitcase Organizer Cubes"	295
"Kharagpur"	"India"	"Google Tri-blend Hoodie Grey"	59
"Not given"	"Czechia"	"YouTube Hard Cover Journal"	7980
"Manchester"	"United Kingdom"	"Google G Noise-reducing Bluetooth Headphones"	101
"Pozuelo de Alarcon"	"Spain"	"YouTube Hard Cover Journal"	1330
"Shibuya"	"Japan"	"Google Men's Vintage Badge Tee Sage"	254
"(not set)"	"United States"	"Google Metallic Notebook Set"	2718
"Not given"	"Slovakia"	"YouTube Custom Decals"	7572
"Bucharest"	"Romania"	"YouTube Custom Decals"	3786
"Not given"	"Peru"	"YouTube Custom Decals"	3786
"(not set)"	"Canada"	"Google Water Resistant Bluetooth Speaker"	183
"St. Louis"	"United States"	"Google Bib Red"	27
"Sherbrooke"	"Canada"	"Nest® Cam Indoor Security Camera - USA"	2139
"Sunnyvale"	"United States"	"Nest® Cam Outdoor Security Camera - USA"	16314
"Ho Chi Minh City"	"Vietnam"	"22 oz YouTube Bottle Infuser"	1465
"Not given"	"Lithuania"	"YouTube Custom Decals"	3786
"Hamburg"	"Germany"	"22 oz YouTube Bottle Infuser"	1465
"(not set)"	"Nepal"	"Google Rucksack"	212
"Hong Kong"	"Hong Kong"	"Spiral Notebook and Pen Set"	3582
"Not given"	"Moldova"	"YouTube Custom Decals"	3786
"Bellingham"	"United States"	"YouTube Custom Decals"	3786
"Neipu Township"	"Taiwan"	"Google Women's Fleece Hoodie"	58
"Salford"	"United Kingdom"	"Google Car Clip Phone Holder"	171
"Detroit"	"United States"	"Google 22 oz Water Bottle"	10075
"Buenos Aires"	"Argentina"	"Sport Bag"	2299
"Fortaleza"	"Brazil"	"Android Luggage Tag"	22
"Not given"	"Hungary"	"YouTube Custom Decals"	3786
"New York"	"United States"	"Google Kick Ball"	30340
"Tampa"	"United States"	"Android Wool Heather Cap Heather/Black"	168
"LaFayette"	"United States"	"Google Men's 100% Cotton Short Sleeve Hero Tee Navy"	15
"Los Angeles"	"Australia"	"Google Twill Cap"	917
"San Diego"	"United States"	"Google Kick Ball"	15170
"Not given"	"Hong Kong"	"Leatherette Journal"	3071
"Yokohama"	"Japan"	"Google Slim Utility Travel Bag"	276
"Santa Monica"	"United States"	"Google Slim Utility Travel Bag"	276
"St. John's"	"Canada"	"Google 2200mAh Micro Charger"	34
"Thessaloniki"	"Greece"	"Red Spiral Google Notebook"	316
"Druid Hills"	"United States"	"Colored Pencil Set"	269
"Not given"	"Haiti"	"Google Men's Short Sleeve Hero Tee Heather"	1
"Jakarta"	"Indonesia"	"22 oz YouTube Bottle Infuser"	2930
"Bandung"	"Indonesia"	"YouTube Men's Short Sleeve Hero Tee Charcoal"	53
"San Salvador"	"El Salvador"	"Google Device Holder Sticky Pad"	49
"Not given"	"United States"	"YouTube Custom Decals"	208230
"Stockholm"	"Sweden"	"Ballpoint Stylus Pen"	769
"(not set)"	"Trinidad & Tobago"	"YouTube Twill Cap"	1429
"Not given"	"Venezuela"	"YouTube Twill Cap"	2858
"Taguig"	"Philippines"	"YouTube RFID Journal"	935
"Courbevoie"	"France"	"Google Men's 100% Cotton Short Sleeve Hero Tee White"	528
"Not given"	"Panama"	"YouTube Custom Decals"	3786
"(not set)"	"Palestine"	"Google Laptop Backpack"	155
"Perth"	"Australia"	"YouTube Custom Decals"	3786
"Lisbon"	"Portugal"	"Google Blackout Cap"	299
"Not given"	"United Kingdom"	"YouTube Custom Decals"	37860
"Beijing"	"China"	"Google Men's Airflow 1/4 Zip Pullover Lapis"	16
"Kansas City"	"United States"	"Google Women's Short Sleeve Hero Tee Red Heather"	11
"Not given"	"Sri Lanka"	"YouTube Custom Decals"	3786
"Not given"	"Serbia"	"YouTube Twill Cap"	2858
"Not given"	"Ghana"	"Google Men's 100% Cotton Short Sleeve Hero Tee White"	528
"Not given"	"Albania"	"22 oz YouTube Bottle Infuser"	1465
"Nashville"	"United States"	"Nest® Learning Thermostat 3rd Gen-USA - Stainless Steel"	1886
"Dublin"	"Netherlands"	"Galaxy Screen Cleaning Cloth"	844
"Cupertino"	"United States"	"Nest® Cam Indoor Security Camera - USA"	2139
"Vancouver"	"United States"	"Google Women's Fleece Hoodie"	0
"(not set)"	"Latvia"	"YouTube RFID Journal"	935
"Cluj-Napoca"	"Romania"	"Google Men's 100% Cotton Short Sleeve Hero Tee Black"	62
"Longtan District"	"Taiwan"	"26 oz Double Wall Insulated Bottle"	845
"Not given"	"Bosnia & Herzegovina"	"You Tube Toddler Short Sleeve Tee Red"	12
"Not given"	"Canada"	"Google 22 oz Water Bottle"	17884
"Not given"	"Taiwan"	"YouTube Custom Decals"	3786
"Sydney"	"Australia"	"YouTube Custom Decals"	7572
"Not given"	"Oman"	"YouTube Hard Cover Journal"	1330
"Wrexham"	"United Kingdom"	"Google Laptop and Cell Phone Stickers"	1033
"Asuncion"	"Paraguay"	"Google Men's 100% Cotton Short Sleeve Hero Tee Navy"	15
"Not given"	"Pakistan"	"22 oz YouTube Bottle Infuser"	5860
"Not given"	"Denmark"	"YouTube Hard Cover Journal"	6650
"Nairobi"	"Kenya"	"Google Flashlight"	9
"Milpitas"	"United States"	"Crunch Noise Dog Toy"	262
"Not given"	"Nigeria"	"Google Twill Cap"	917
"Mountain View"	"United States"	"Nest® Cam Indoor Security Camera - USA"	51336
"Cape Town"	"South Africa"	"Google Men's Pullover Hoodie Grey"	25
"(not set)"	"United Kingdom"	"Basecamp Explorer Powerbank Flashlight"	200
"Munich"	"Germany"	"YouTube Custom Decals"	3786
"Calgary"	"Canada"	"YouTube Leatherette Notebook Combo"	1148
"Minato"	"Japan"	"Google Kick Ball"	15170
"(not set)"	"Brazil"	"Google Men's Vintage Badge Tee Black"	433
"Houston"	"United States"	"Google Sunglasses"	4204
"Not given"	"Bulgaria"	"YouTube Custom Decals"	3786
"Not given"	"Kyrgyzstan"	"Rocket Flashlight"	123
"Gurgaon"	"India"	"Google 22 oz Water Bottle"	8942
"Madrid"	"Spain"	"SPF-15 Slim & Slender Lip Balm"	7364
"Not given"	"Somalia"	"YouTube Men's Short Sleeve Hero Tee White"	50
"Redwood City"	"United States"	"Nest® Cam Indoor Security Camera - USA"	2139
"Council Bluffs"	"United States"	"Google Kick Ball"	15170
"Bangkok"	"United States"	"Android 5-Panel Low Cap"	7
"Pittsburgh"	"United States"	"Nest® Cam Outdoor Security Camera - USA"	2719
"Marlboro"	"United States"	"Google Men's Microfiber 1/4 Zip Pullover Blue/Indigo"	0
"Oxford"	"United Kingdom"	"Google Water Resistant Bluetooth Speaker"	183
"Doha"	"Qatar"	"Google Men's 100% Cotton Short Sleeve Hero Tee Black"	62
"Not given"	"Philippines"	"Spiral Notebook and Pen Set"	7164
"Los Angeles"	"United States"	"Google Kick Ball"	15170
"Quezon City"	"Philippines"	"Seat Pack Organizer"	160
"Helsinki"	"Finland"	"Android Onesie Gold"	31
"Not given"	"Qatar"	"Google 5-Panel Cap"	47
"Akron"	"United States"	"Google Men's 100% Cotton Short Sleeve Hero Tee Navy"	15
"Not given"	"Switzerland"	"YouTube Custom Decals"	3786
"Not given"	"Kuwait"	"Google 17oz Stainless Steel Sport Bottle"	716
"Zagreb"	"Croatia"	"Google Men's Watershed Full Zip Hoodie Grey"	108
"Not given"	"Russia"	"YouTube Twill Cap"	5716
"Not given"	"Ecuador"	"YouTube RFID Journal"	935
"Not given"	"Spain"	"22 oz YouTube Bottle Infuser"	4395
"Colombo"	"Sri Lanka"	"Google Men's 100% Cotton Short Sleeve Hero Tee White"	528
"Not given"	"Puerto Rico"	"YouTube Custom Decals"	3786




**Question 5: Can we summarize the impact of revenue generated from each city/country?**

SQL Queries:
SELECT city, country, SUM(revenue) AS total_revenue
FROM your_table_name
GROUP BY city, country
ORDER BY total_revenue DESC;

Answer:
"Not given"	"United States"	40298133.75
"Mountain View"	"United States"	29923011.39
"Sunnyvale"	"United States"	8310431.86
"San Francisco"	"United States"	8299135.85
"Palo Alto"	"United States"	7422479.88
"New York"	"United States"	7145857.25
"San Jose"	"United States"	3834088.90
"London"	"United Kingdom"	3182577.70
"Not given"	"United Kingdom"	3065952.17
"Chicago"	"United States"	2879320.27
"Not given"	"Canada"	2862592.28
"Seattle"	"United States"	2670826.50
"Santa Clara"	"United States"	2469951.35
"Not given"	"Italy"	1987402.99
"Los Angeles"	"United States"	1964236.47
"Austin"	"United States"	1785600.15
"Not given"	"Germany"	1547458.96
"Not given"	"India"	1132812.08
"Atlanta"	"United States"	789972.75
"Pittsburgh"	"United States"	765106.14
"Not given"	"Spain"	732936.99
"Not given"	"Sweden"	727921.82
"Not given"	"Japan"	721089.28
"Cambridge"	"United States"	720840.05
"Hong Kong"	"Hong Kong"	703711.46
"(not set)"	"Taiwan"	689614.83
"Not given"	"Netherlands"	689528.14
"Ann Arbor"	"United States"	634570.05
"San Bruno"	"United States"	631450.75
"Dublin"	"Ireland"	628892.34
"Mumbai"	"India"	626552.94
"Not given"	"France"	622179.55
"Not given"	"Mexico"	604161.31
"Mexico City"	"Mexico"	584614.27
"Kirkland"	"United States"	555955.94
"Cupertino"	"United States"	552639.56
"Bogota"	"Colombia"	543560.96
"Not given"	"Honduras"	541305.97
"Toronto"	"Canada"	532724.82
"Not given"	"Brazil"	509942.93
"Irvine"	"United States"	505119.91
"Not given"	"Morocco"	493041.62
"Sydney"	"Australia"	484928.97
"Bellingham"	"United States"	477148.14
"Not given"	"Czechia"	469126.01
"Redwood City"	"United States"	436742.28
"Sherbrooke"	"Canada"	431339.01
"Menlo Park"	"United States"	431320.66
"Phoenix"	"United States"	430061.70
"Not given"	"Australia"	427593.78
"Melbourne"	"Australia"	406585.79
"San Diego"	"United States"	402077.77
"Hyderabad"	"India"	396283.62
"Chennai"	"India"	378170.85
"Not given"	"Russia"	371911.97
"(not set)"	"Singapore"	361889.35
"Not given"	"Denmark"	333626.72
"Not given"	"Philippines"	325631.21
"Salem"	"United States"	284574.90
"Nashville"	"United States"	281014.00
"Washington"	"United States"	263925.91
"Not given"	"Indonesia"	255707.09
"(not set)"	"Hong Kong"	248952.30
"Madrid"	"Spain"	235097.94
"Bengaluru"	"India"	230439.58
"Not given"	"Turkey"	214618.66
"Not given"	"Switzerland"	210520.51
"Houston"	"United States"	203601.14
"Singapore"	"Singapore"	201827.96
"Not given"	"Pakistan"	200553.51
"Not given"	"Taiwan"	192974.63
"Not given"	"New Zealand"	189377.93
"Not given"	"Slovakia"	188537.00
"Not given"	"South Africa"	188364.65
"(not set)"	"United States"	187317.66
"Not given"	"Ukraine"	182760.37
"Fremont"	"United States"	180135.38
"Not given"	"Belgium"	178321.86
"Tel Aviv-Yafo"	"Israel"	170097.33
"Paris"	"France"	170089.26
"Osaka"	"Japan"	169707.38
"Minato"	"Japan"	169602.12
"Montreal"	"Canada"	166972.14
"Dallas"	"United States"	160880.09
"Bangkok"	"Thailand"	158683.91
"Sao Paulo"	"Brazil"	155169.00
"(not set)"	"India"	149146.99
"New Delhi"	"India"	147791.43
"Not given"	"Greece"	139061.83
"Not given"	"Poland"	133615.01
"Not given"	"Portugal"	126562.82
"Not given"	"Colombia"	120844.41
"Not given"	"Argentina"	118279.04
"Not given"	"Malaysia"	115786.42
"Istanbul"	"Turkey"	113408.25
"Not given"	"Venezuela"	111390.66
"Not given"	"Norway"	106604.73
"Not given"	"Austria"	105035.84
"Zurich"	"Switzerland"	104955.07
"Not given"	"Romania"	104325.91
"Not given"	"Chile"	94789.64
"Charlotte"	"United States"	88770.57
"Munich"	"Germany"	88718.86
"Philadelphia"	"United States"	87477.85
"Pune"	"India"	86172.07
"Seoul"	"South Korea"	85085.32
"Not given"	"Israel"	82860.02
"Not given"	"Bulgaria"	82697.51
"Kiev"	"Ukraine"	80862.33
"Rome"	"Italy"	79536.28
"Kolkata"	"India"	79416.22
"Kuala Lumpur"	"Malaysia"	78718.48
"Not given"	"Ireland"	76759.06
"Not given"	"South Korea"	76546.04
"Not given"	"China"	76055.91
"Not given"	"Vietnam"	75668.92
"Not given"	"Peru"	74936.18
"(not set)"	"Not given"	74730.29
"Not given"	"Bangladesh"	73726.96
"Redmond"	"United States"	73680.11
"Not given"	"Panama"	72928.34
"Not given"	"Thailand"	72094.36
"Boston"	"United States"	71897.12
"Warsaw"	"Poland"	67888.46
"Jakarta"	"Indonesia"	67023.01
"Hamburg"	"Germany"	63897.92
"Not given"	"Guatemala"	62312.61
"Barcelona"	"Spain"	61461.94
"Dubai"	"United Arab Emirates"	60382.96
"Milan"	"Italy"	60218.75
"Zhongli District"	"Taiwan"	59334.32
"Not given"	"Serbia"	56588.98
"Not given"	"Hungary"	56529.48
"Saint Petersburg"	"Russia"	55636.73
"Bucharest"	"Romania"	53202.23
"Not given"	"Slovenia"	52721.69
"Not given"	"Dominican Republic"	52653.40
"Moscow"	"Russia"	51736.05
"Stockholm"	"Sweden"	50927.67
"Taguig"	"Philippines"	50706.12
"Santiago"	"Chile"	49816.65
"Not given"	"Saudi Arabia"	46817.04
"Not given"	"Uruguay"	46655.41
"Ahmedabad"	"India"	46294.89
"Vancouver"	"Canada"	46167.25
"Not given"	"Puerto Rico"	45093.04
"Amsterdam"	"Netherlands"	44272.96
"Not given"	"Kuwait"	44084.73
"Berlin"	"Germany"	42025.86
"Not given"	"Ecuador"	41835.96
"Denver"	"United States"	41490.65
"Shinjuku"	"Japan"	41205.43
"Not given"	"Croatia"	40754.50
"Athens"	"Greece"	40671.58
"Not given"	"Laos"	39873.40
"Indore"	"India"	38888.55
"(not set)"	"Bangladesh"	38668.59
"(not set)"	"Greece"	38562.01
"Riyadh"	"Saudi Arabia"	37419.86
"La Victoria"	"Peru"	37216.78
"(not set)"	"Peru"	36619.70
"Detroit"	"United States"	36110.08
"(not set)"	"Trinidad & Tobago"	35641.41
"Brno"	"Czechia"	35050.04
"Not given"	"Costa Rica"	34749.33
"Not given"	"Hong Kong"	34529.90
"Gurgaon"	"India"	34203.49
"Not given"	"Nigeria"	34022.19
"Not given"	"Egypt"	34001.53
"Not given"	"Lithuania"	33447.41
"Not given"	"Georgia"	32576.68
"Ho Chi Minh City"	"Vietnam"	32131.58
"Perth"	"Australia"	30979.21
"Brisbane"	"Australia"	30888.55
"Hanoi"	"Vietnam"	30222.12
"Buenos Aires"	"Argentina"	29415.93
"Not given"	"Latvia"	29198.34
"Not given"	"Ethiopia"	27961.22
"San Antonio"	"United States"	27778.18
"Not given"	"Papua New Guinea"	27470.84
"Not given"	"United Arab Emirates"	27332.38
"Not given"	"Singapore"	27058.46
"Not given"	"Cambodia"	26044.89
"Prague"	"Czechia"	26003.34
"Oakland"	"United States"	25216.62
"Boulder"	"United States"	24597.96
"Council Bluffs"	"United States"	24320.22
"Not given"	"Sri Lanka"	24081.97
"Vienna"	"Austria"	23814.86
"Eau Claire"	"United States"	23646.44
"Not given"	"Finland"	23565.15
"Not given"	"Tunisia"	23504.08
"Colombo"	"Sri Lanka"	23132.68
"Karachi"	"Pakistan"	23120.07
"Pozuelo de Alarcon"	"Spain"	21745.76
"University Park"	"United States"	21497.85
"Not given"	"Botswana"	21497.85
"Longtan District"	"Taiwan"	21116.55
"Yokohama"	"Japan"	21033.49
"Not given"	"Oman"	19936.70
"Not given"	"Malta"	18914.61
"Not given"	"Macau"	18781.95
"(not set)"	"Latvia"	18690.65
"Not given"	"Lebanon"	18690.65
"Not given"	"Sudan"	18690.65
"Mississauga"	"Canada"	18399.79
"Orlando"	"United States"	17734.99
"Not given"	"Bolivia"	17616.30
"Rexburg"	"United States"	17584.74
"South San Francisco"	"United States"	16995.62
"Rio de Janeiro"	"Brazil"	16697.61
"(not set)"	"Indonesia"	16318.80
"Kalamazoo"	"United States"	16115.97
"Not given"	"Algeria"	15992.59
"Not given"	"Tanzania"	15704.71
"Culiacan"	"Mexico"	15685.40
"Santa Fe"	"Argentina"	15608.17
"(not set)"	"Palestine"	15498.45
"Bellflower"	"United States"	15068.28
"Auckland"	"New Zealand"	14969.96
"(not set)"	"Nepal"	14837.88
"Makati"	"Philippines"	14782.97
"Manchester"	"United Kingdom"	14744.99
"Calgary"	"Canada"	13976.22
"Milpitas"	"United States"	13752.09
"Jacksonville"	"United States"	13238.47
"Not given"	"Estonia"	13177.88
"Courbevoie"	"France"	13169.04
"Quebec City"	"Canada"	13072.53
"Tempe"	"United States"	12613.11
"San Francisco"	"France"	12470.01
"Bhubaneswar"	"India"	12470.01
"Zagreb"	"Croatia"	11878.92
"Jaipur"	"India"	11838.21
"Not given"	"Martinique"	11666.23
"Not given"	"Bahrain"	11536.21
"Westville"	"South Africa"	11472.01
"(not set)"	"Réunion"	11391.24
"Not given"	"Côte d’Ivoire"	11225.72
"Burnaby"	"Canada"	10695.98
"Montevideo"	"Uruguay"	10680.15
"Not given"	"Ghana"	10293.09
"Not given"	"Myanmar (Burma)"	10130.69
"(not set)"	"Bahamas"	10077.83
"Los Angeles"	"Australia"	10077.83
"Stanford"	"United States"	9966.22
"New York"	"Canada"	9966.22
"Not given"	"Jamaica"	9966.22
"Not given"	"Mauritius"	9740.91
"Monterrey"	"Mexico"	9202.21
"Not given"	"Macedonia (FYROM)"	9189.85
"Timisoara"	"Romania"	9137.68
"Not given"	"Iraq"	9027.48
"Not given"	"Albania"	8857.69
"Vladivostok"	"Russia"	8810.49
"Oviedo"	"United States"	8522.20
"Rosario"	"Argentina"	8222.67
"(not set)"	"Brazil"	8222.67
"Singapore"	"France"	8222.67
"Not given"	"Belarus"	8068.45
"(not set)"	"Bosnia & Herzegovina"	8024.52
"Sakai"	"Japan"	8024.52
"(not set)"	"Serbia"	7910.35
"Not given"	"Nepal"	7823.08
"Not given"	"Cyprus"	7644.87
"(not set)"	"San Marino"	7554.86
"Not given"	"Mali"	7534.14
"Not given"	"Moldova"	7534.14
"Not given"	"Montenegro"	7534.14
"Cork"	"Ireland"	7534.14
"(not set)"	"Côte d’Ivoire"	7534.14
"Richardson"	"United States"	7398.15
"(not set)"	"Kosovo"	7356.67
"Medellin"	"Colombia"	7206.46
"Avon"	"United States"	6945.01
"Not given"	"Kazakhstan"	6757.66
"Montreuil"	"France"	6712.47
"Norfolk"	"United States"	6695.94
"East Lansing"	"United States"	6599.34
"Not given"	"Jordan"	6487.05
"Quezon City"	"Philippines"	6467.99
"Oxford"	"United Kingdom"	6403.17
"(not set)"	"Canada"	6403.17
"Glasgow"	"United Kingdom"	6403.17
"Sandton"	"South Africa"	6403.17
"Kharagpur"	"India"	6319.08
"Edmonton"	"Canada"	6244.61
"Poznan"	"Poland"	6152.53
"(not set)"	"Switzerland"	6050.00
"(not set)"	"Sint Maarten"	6050.00
"Stuttgart"	"Germany"	5989.86
"(not set)"	"United Kingdom"	5957.37
"Adelaide"	"Australia"	5939.46
"Belo Horizonte"	"Brazil"	5908.16
"Sacramento"	"United States"	5678.01
"Lisbon"	"Portugal"	5678.01
"Shibuya"	"Japan"	5672.96
"Ghent"	"Belgium"	5390.49
"(not set)"	"Philippines"	5390.49
"Not given"	"Armenia"	5390.49
"Villeneuve-d'Ascq"	"France"	5287.70
"Kitchener"	"Canada"	4747.96
"Manila"	"Philippines"	4736.85
"Ashburn"	"United States"	4334.25
"Maracaibo"	"Venezuela"	4333.61
"Budapest"	"Hungary"	4314.78
"Indianapolis"	"United States"	4229.50
"Tampa"	"United States"	4198.32
"Goose Creek"	"United States"	4198.32
"Santa Monica"	"United States"	4137.24
"Mountain View"	"Australia"	3959.67
"Not given"	"Maldives"	3959.67
"Lahore"	"Pakistan"	3703.82
"Patna"	"India"	3494.46
"Thessaloniki"	"Greece"	3480.57
"Portland"	"United States"	3439.10
"Toronto"	"United States"	3358.32
"Not given"	"El Salvador"	3287.16
"Kovrov"	"Russia"	3247.42
"Neipu Township"	"Taiwan"	3247.42
"Wrexham"	"United Kingdom"	3088.67
"Not given"	"Uganda"	3088.67
"Mountain View"	"Japan"	2867.49
"Minneapolis"	"United States"	2658.60
"San Mateo"	"United States"	2603.92
"Hayward"	"United States"	2601.63
"Not given"	"Brunei"	2573.09
"Not given"	"Nicaragua"	2409.32
"Petaling Jaya"	"Malaysia"	2393.93
"(not set)"	"Japan"	2377.27
"Not given"	"Bahamas"	2369.21
"Iasi"	"Romania"	2369.21
"Not given"	"Gibraltar"	2369.21
"Not given"	"Jersey"	2359.41
"South El Monte"	"United States"	2327.63
"Not given"	"Kenya"	2309.46
"Lake Oswego"	"United States"	2270.08
"Mexico City"	"United States"	2238.40
"Las Vegas"	"United States"	2211.20
"Nagoya"	"Japan"	2177.78
"The Dalles"	"United States"	2055.67
"Izmir"	"Turkey"	1970.84
"Greer"	"United States"	1949.74
"Not given"	"Zimbabwe"	1679.56
"Pleasanton"	"United States"	1646.70
"Chico"	"United States"	1539.56
"(not set)"	"Thailand"	1459.27
"Lucknow"	"India"	1379.34
"Parsippany-Troy Hills"	"United States"	1349.82
"Dublin"	"Netherlands"	1341.96
"Not given"	"Barbados"	1299.75
"Yokohama"	"United States"	1299.75
"Cape Town"	"South Africa"	1299.75
"Chuo"	"Japan"	1299.35
"San Francisco"	"Japan"	1299.35
"London"	"United States"	1267.68
"Ipoh"	"Malaysia"	1267.00
"Not given"	"Qatar"	1222.38
"Salford"	"United Kingdom"	1195.29
"Appleton"	"United States"	1121.34
"Beijing"	"China"	1119.84
"Istanbul"	"Hungary"	1085.37
"Hong Kong"	"United States"	1085.37
"Doha"	"Qatar"	1053.38
"Cluj-Napoca"	"Romania"	1053.38
"Brussels"	"Belgium"	1053.38
"Marseille"	"France"	1053.38
"Jersey City"	"United States"	1044.45
"Nanded"	"India"	1006.47
"Bandung"	"Indonesia"	1006.47
"Kharkiv"	"Ukraine"	968.49
"Madison"	"United States"	919.08
"Ottawa"	"Canada"	868.49
"Egham"	"United Kingdom"	849.50
"Not given"	"Somalia"	849.50
"Druid Hills"	"United States"	804.31
"Antwerp"	"Belgium"	804.31
"Wellesley"	"United States"	804.31
"St. John's"	"Canada"	781.66
"Frankfurt"	"Germany"	779.35
"Columbia"	"United States"	768.46
"Columbus"	"United States"	766.83
"Helsinki"	"Finland"	743.69
"Oslo"	"Norway"	679.60
"Piscataway Township"	"United States"	679.60
"Vilnius"	"Lithuania"	679.60
"Copenhagen"	"Denmark"	613.77
"Not given"	"Kyrgyzstan"	613.77
"Nairobi"	"Kenya"	599.88
"Berkeley"	"United States"	599.75
"Bilbao"	"Spain"	512.73
"Paris"	"United States"	449.94
"Coventry"	"United Kingdom"	417.78
"St. Louis"	"United States"	323.73
"Forest Park"	"United States"	299.95
"Not given"	"Luxembourg"	287.88
"Asuncion"	"Paraguay"	254.85
"LaFayette"	"United States"	254.85
"Akron"	"United States"	254.85
"Chandigarh"	"India"	254.85
"San Salvador"	"El Salvador"	244.51
"Kansas City"	"United States"	227.88
"(not set)"	"Dominican Republic"	224.97
"Not given"	"Bosnia & Herzegovina"	203.88
"Sapporo"	"Japan"	203.88
"Amsterdam"	"United States"	199.92
"Waterloo"	"Canada"	199.92
"Fortaleza"	"Brazil"	197.78
"Bangkok"	"United States"	132.93
"(not set)"	"Sri Lanka"	59.97
"(not set)"	"Puerto Rico"	56.97
"(not set)"	"Panama"	37.98
"El Paso"	"United States"	37.98
"Not given"	"Haiti"	18.99
"Krakow"	"Poland"	0
"Marlboro"	"United States"	0.00
"Johnson City"	"United States"	0
"Quimper"	"France"	0
"Watford"	"United Kingdom"	0.00
"Wroclaw"	"Poland"	0
"Antalya"	"Turkey"	0.00
"Odessa"	"Ukraine"	0
"(not set)"	"Netherlands"	0
"Esbjerg"	"Denmark"	0
"(not set)"	"Belize"	0
"Belgrade"	"Serbia"	0
"Skopje"	"Macedonia (FYROM)"	0
"Bratislava"	"Slovakia"	0.00
"Not given"	"Iceland"	0
"Gothenburg"	"Sweden"	0
"(not set)"	"Iceland"	0.00
"Not given"	"French Polynesia"	0
"Raleigh"	"United States"	0
"Nice"	"France"	0
"Panama City"	"United States"	0.00
"Charlottetown"	"Canada"	0
"Westlake Village"	"United States"	0.00
"Rotterdam"	"Netherlands"	0.00
"(not set)"	"Sudan"	0
"Alexandria"	"Egypt"	0
"Bordeaux"	"France"	0.00
"Not given"	"Rwanda"	0.00
"Amã"	"Jordan"	0
"Vancouver"	"United States"	0.00
"Not given"	"Not given"	0.00
"Fort Worth"	"United States"	0.00
"Chiyoda"	"Japan"	0.00
