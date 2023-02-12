# Lab Report 3
Different ways to use the `grep` command:  
1. `grep -c`  will print a count of the lines that match the specified pattern
2. `grep -h` will display the lines but not the name of the file
3. `grep -A n` will print the searched line and n lines after the result
4. `grep -n` will show the matched lines and the line numbers

Source: [grep commands](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)  

## Examples using `grep -c`  

### Example 1  
Input:  
`grep -c "Bahamas" travel_guides/berlitz2/*.txt`  
Output:    
`travel_guides/berlitz2/Algarve-History.txt:0
travel_guides/berlitz2/Algarve-Intro.txt:0
travel_guides/berlitz2/Algarve-WhatToDo.txt:0
travel_guides/berlitz2/Algarve-WhereToGo.txt:0
travel_guides/berlitz2/Amsterdam-History.txt:0
travel_guides/berlitz2/Amsterdam-Intro.txt:0
travel_guides/berlitz2/Amsterdam-WhatToDo.txt:0
travel_guides/berlitz2/Amsterdam-WhereToGo.txt:0
travel_guides/berlitz2/Athens-History.txt:0
travel_guides/berlitz2/Athens-Intro.txt:0
travel_guides/berlitz2/Athens-WhatToDo.txt:0
travel_guides/berlitz2/Athens-WhereToGo.txt:0
travel_guides/berlitz2/Bahamas-History.txt:23
travel_guides/berlitz2/Bahamas-Intro.txt:11
travel_guides/berlitz2/Bahamas-WhatToDo.txt:16
travel_guides/berlitz2/Bahamas-WhereToGo.txt:34
travel_guides/berlitz2/Bali-History.txt:0
travel_guides/berlitz2/Bali-WhatToDo.txt:0
travel_guides/berlitz2/Bali-WhereToGo.txt:0
travel_guides/berlitz2/Barcelona-History.txt:0
travel_guides/berlitz2/Barcelona-WhatToDo.txt:0
travel_guides/berlitz2/Barcelona-WhereToGo.txt:0
travel_guides/berlitz2/Beijing-History.txt:0
travel_guides/berlitz2/Beijing-WhatToDo.txt:0
travel_guides/berlitz2/Beijing-WhereToGo.txt:0
travel_guides/berlitz2/Berlin-History.txt:0
travel_guides/berlitz2/Berlin-WhatToDo.txt:0
travel_guides/berlitz2/Berlin-WhereToGo.txt:0
travel_guides/berlitz2/Bermuda-WhatToDo.txt:0
travel_guides/berlitz2/Bermuda-WhereToGo.txt:0
travel_guides/berlitz2/Bermuda-history.txt:0
travel_guides/berlitz2/Boston-WhereToGo.txt:0
travel_guides/berlitz2/Budapest-History.txt:0
travel_guides/berlitz2/Budapest-WhatToDo.txt:0
travel_guides/berlitz2/Budapest-WhereoGo.txt:0
travel_guides/berlitz2/California-History.txt:0
travel_guides/berlitz2/California-WhatToDo.txt:0
travel_guides/berlitz2/California-WhereToGo.txt:0
travel_guides/berlitz2/Canada-History.txt:0
travel_guides/berlitz2/Canada-WhereToGo.txt:1
travel_guides/berlitz2/CanaryIslands-History.txt:0
travel_guides/berlitz2/CanaryIslands-WhatToDo.txt:0
travel_guides/berlitz2/CanaryIslands-WhereToGo.txt:0
travel_guides/berlitz2/Cancun-History.txt:0
travel_guides/berlitz2/Cancun-WhatToDo.txt:0
travel_guides/berlitz2/Cancun-WhereToGo.txt:0
travel_guides/berlitz2/China-History.txt:0
travel_guides/berlitz2/China-WhatToDo.txt:0
travel_guides/berlitz2/China-WhereToGo.txt:0
travel_guides/berlitz2/Costa-History.txt:0
travel_guides/berlitz2/Costa-WhatToDo.txt:0
travel_guides/berlitz2/Costa-WhereToGo.txt:0
travel_guides/berlitz2/CostaBlanca-History.txt:0
travel_guides/berlitz2/CostaBlanca-WhatToDo.txt:0
travel_guides/berlitz2/Crete-History.txt:0
travel_guides/berlitz2/Crete-WhatToDo.txt:0
travel_guides/berlitz2/Crete-WhereToGo.txt:0
travel_guides/berlitz2/CstaBlanca-WhereToGo.txt:0
travel_guides/berlitz2/Cuba-History.txt:0
travel_guides/berlitz2/Cuba-WhatToDo.txt:0
travel_guides/berlitz2/Cuba-WhereToGo.txt:0
travel_guides/berlitz2/Nepal-History.txt:0
travel_guides/berlitz2/Nepal-WhatToDo.txt:0
travel_guides/berlitz2/Nepal-WhereToGo.txt:0
travel_guides/berlitz2/NewOrleans-History.txt:0
travel_guides/berlitz2/Paris-WhatToDo.txt:0
travel_guides/berlitz2/Paris-WhereToGo.txt:0
travel_guides/berlitz2/Poland-History.txt:0
travel_guides/berlitz2/Poland-WhatToDo.txt:0
travel_guides/berlitz2/Portugal-History.txt:0
travel_guides/berlitz2/Portugal-WhatToDo.txt:0
travel_guides/berlitz2/Portugal-WhereToGo.txt:0
travel_guides/berlitz2/PuertoRico-History.txt:0
travel_guides/berlitz2/PuertoRico-WhatToDo.txt:0
travel_guides/berlitz2/PuertoRico-WhereToGo.txt:0
travel_guides/berlitz2/Vallarta-History.txt:0
travel_guides/berlitz2/Vallarta-WhatToDo.txt:0
travel_guides/berlitz2/Vallarta-WhereToGo.txt:0`  

In this example, we are able to search through all of the files in `/berlitz2` and list out how many times each file uses the word "Bahamas". This can be useful when trying to find out how many times a word is used in multiple files.  

### Example 2  
Input:  
`grep -c "the" travel_guides/berlitz2/Vallarta-WhereToGo.txt`  
Output:  
`111`  

In this example, we are only looking at how many times the word "the" comes up in the file `Vallarta-WhereToGo.txt`.  


## Examples using `grep -h`
### Example 1  
Input:  
`grep -h "what" travel_guides/berlitz2/Vallarta-WhereToGo.txt`  
Output:  
`The cultural scene has blossomed as well, with Vallarta — as it is called by the locals — now considered among the country’s leading art centers. Especially during the winter months, an almost constant succession of gallery openings and exhibitions attracts creative talent from throughout the Americas. The culinary community has taken numerous awards and accolades back to this seaside town, where more than 250 restaurants offer gourmands their own piece of paradise. Yet what makes this place overwhelmingly attractive is its total lack of pretense and completely comfortable ambiance — it remains down-to-earth, genuinely casual, and simply irresistible.
The best known image of Puerto Vallarta is the Iglesia de Guadalupe (Guadalupe Church), dedicated to the Virgin of Guadalupe, and topped by a copy of the crown worn by Empress Carlota in the 1860s. Wife of Emperor Maximillian, the only emperor of Mexico to be appointed by a foreign power, she is considered to be a tragic heroine. Golden angels hold up the bell tower, and the interior is decorated with a few muted murals. The church overlooks Puerto Vallarta’s plaza with its central bandstand and adjacent Palacio Municipal (City Hall). This plaza is representative of plazas throughout Mexico; what reminds you that you are in an international tourist town are the surrounding signs for Burger King, Subway, and Hooters.
Zihuatanejo became popular among beachcombers from abroad because it had what they wanted: a sparkling bay divided into intimate stretches of sand by outcroppings of rock and wooded knolls, plus simple pleasures that included swimming, sunning, and the freshest of fruit and seafood. Cheap beer and rum were an added bonus.
The first beach in Ixtapa, coming from Zihua is Playa Hermosa, which can only be accessed through the Westin Hotel. This small beach is dramatically framed by rock formations. The surf varies seasonally from minimal to quite rough, and has become somewhat of a private beach for Westin’s guests.
Also known as Acapulco Viejo (Old Acapulco), this intriguing area is the part of Acapulco that originally attracted the glamorous jet-setters of days past, and which, today, is experiencing something of a renaissance. For years, travelers to Acapulco have dismissed this section of town, which includes the Península de las Playas and extends east to Papagayo Park, not knowing what they’re missing. Currently, it is where Acapulco’s most value-priced hotels are found, along with budget dining choices and the typical businesses and services of any sizable city.
An additional 8 km (5 miles) down the coast road from Mazunte is the dusty beach village Puerto Angel, once considered a prime destination for backpackers and budget travelers. This place truly is a “sleepy little fishing vill age,” though a succession of natural disasters (hurricane and earthquake damage in the past four years) have made it less desirable for long-term stays. In addition, the Naval Base is what now dominates the once picturesque central town beach. The best place to spend some relaxation time is at one of the beachfront restaurants at Playa Panteón, the lively cove located in front of the town cemetery (panteón means “cemetery”).
It’s biggest draw are the 36 beaches spread across the 35 km (22 miles) of coastline and nine bays, most of them still undeveloped. The fact that the area has been slow to catch on has resulted in a curious mix of ultra-modern infrastructure, and unspoiled natural areas. Huatulco has what it takes to attract visitors — including golf, tennis, water sports, fishing, a few restaurants and night spots, luxury accommodations, and direct flights from selected US cities — but hasn’t developed its own distinct personality yet. For now, Huatulco is ideal for those who want to enjoy the beauty of nature during the day, then retreat to the well-appointed comfort of a luxury hotel by night.`  

Here we used `grep -h` to only show the lines that contain the word "what". This can be useful if we don't care about the file name and want to find out the context of the word. 

### Example 2  
Input:  
`grep -h "political evolution" travel_guides/berlitz2/Cuba-History.txt`  
Output:  
`Washington remained fundamentally opposed to Cuba’s political evolution and sought to isolate Castro in Latin America. Soon after the Bay of Pigs, Castro declared himself a Marxist-Leninist. Castro had not displayed any Communist inclinations in the 1950s, and some suggest that US aggression pushed him to ingratiate himself with the powerful Soviet Union and its Eastern block of potential trading partners. By the end of the 1980s, more than 80 percent of Cuban trade was with the USSR, which also provided Cuba with a subsidy of state support worth an estimated US$5 billion annually.`  

In this example, `grep -h` was used to search through a different file for the words "political evoluion".   

## Examples using `grep -A n`
### Example 1
Input:  
`grep -A 2 "Bahamas" travel_guides/berlitz2/Canada-WhereToGo.txt`  
Output:  
`Without detracting from the significance of Columbus’s landing on the Bahamas, Newfoundland can lay a just claim to being the true beginning of Europe’s adventure in North America. Anyone seeking to understand Canada’s role in shaping North America should spare a few days for this bracing province of hardy fisherfolk — first Canadian land to be “found” and last to join the Confederation (incorporating Labrador), in 1949. The land and seascapes are impressively rugged and the spirited people a sheer delight. Life in isolated fishing communities has given the Newfies a keen sense of local identity. Citizens of the capital of St. John’s are “townees,” those on the outskirts “bay-men,” and the towns beyond are known as “outports.” “Canadian” is still reserved for a mainlander.
“Seek ye first the Kingdom of God,” says the provincial motto. “But on your way, look out for Newfoundland,” seems to have been the slogan of the old North Atlantic navigators, from the good Irish Abbot Brendan in the sixth century and the wild Norsemen in the 11th, to all the Basque, French, Spanish, and Portuguese fishermen who preceded explorer John Cabot, paid £10 by Henry VII for finding “the new isle” in 1497.
It was the fishermen who really knew what the island was worth — the Grand Banks to the east of Newfoundland are the richest breeding ground of cod in the world. For centuries, the island existed only for its offshore fish. Any permanent settlement was actively discouraged, so as not to compete with Britain’s West Country merchants. Even after the first serious colonization of the 18th century, the forests of the interior were exploited just for building fishermen’s cottages and their ships. No towns were built away from the coast.`  

In this example, `grep -A n` is used to find a specific word and the context surrounding it like with `grep -h`, but we can choose how many lines after it are shown. In this case, it's two lines.  

### Example 2
Input:  
`grep -A 1 "somewhat" travel_guides/berlitz2/China-WhereToGo.txt`  
Output:  
`Datong itself is a rather poor coal-mining and industrial city, somewhat behind the times, set on a loess plateau 1,000 m (3,280 ft) above sea level. The summers are short here on the edge of Inner Mongolia, and winters are glacial. It’s not the sort of place poets would eulogize, yet for nearly a century (398–494) it served as the capital of the Northern Wei Dynasty.
Three monasteries and a famous dragon screen recall Datong’s once stately history. The Nine Dragon Wall (Jiulongbi), a Ming landmark (1392), stands in the old part of town among the narrow streets lined by single-story houses. This is said to be the largest and oldest screen of its type anywhere in China, at 457 m (150 ft) certainly longer than the more famous version in the Forbidden City. The ceramic mural shows nine dragons, each in a different dynamic pose. When the sun reflects on the pool that runs along the base of the wall, the glazed tile figures flash to life.`  

In this example, `grep -A n` was used to find the word "somewhat" and the singular line that comes after. 

## Examples using `grep -n`
### Example 1
Input:  
`grep -n "Santa Cruz" travel_guides/berlitz2/CanaryIslands-WhereToGo.txt`  
Output:  
`13:Santa Cruz de Tenerife
14:The capital of Tenerife and the administrative center for the westerly Canaries, Santa Cruz is not a city in which tourists spend a great deal of time. The main square is the Plaza de España, in the middle of which stands a four-sided cross, a memorial to the dead of the Spanish Civil War. The huge, drab, gray building adjacent to the Plaza is the Cabildo Insular (local government headquarters) which also houses the tourist office and the Museo Arqueológico, with important exhibits illustrating the life and death rituals of Guanche society (see page 13). The museum is open Tuesday–Sunday 10am–8pm and the entrance fee is a mere 400 pesetas (free on Sundays). Back on the seafront, discover the Iglesia Matriz de la Concepción (Church of the Immaculate Conception). Dating from the early 16th century, this is the town’s most important historical building and contains several interesting relics, including Nelson’s faded battle flag.
31:The entrance to the National Park is El Portillo de las Cañadas, where there is a visitor center (open daily 9am–4pm). If you wish to walk in the park, pick up a leaflet or ask for information about the daily guided walks. Note that during winter the environment can become quite harsh, and you should never undertake walks without consulting staff at the visitor center first. At this point it is quite likely that you will be in the clouds; temperatures are very low, and in winter there may well be snow on the ground. The landscape becomes very lunar-like; it was around here that some of the filming for Planet of the Apes took place. The ascent to the top of Mount Teide can be made by climbing, or by the new cable car (teleférico), an eight-minute ride (open daily 9am–4pm, admission: 2,500 ptas, r15.03). Most visitors choose the cable car, but it’s worth noting that even after leaving the cable car it is still a good climb to the summit at 3,717 m (12,195 ft). However, if you really want to venture that far you have to go in person and with a photocopy of your passport, to the Office of the Parque Nacional del Teide (Calle Emilio Calzadilla, 5, 38002 Santa Cruz de Tenerife). Even then, there is a daily limit of just 50 people, for conservation sake, allowed up the last 200 m (219 yards) to the summit. Once there, you should be able to count off all the other Canary Islands and, on a good day, see North Africa. Impressive as Teide is, it is basically no more than a peak on the edge of a giant volcano which long ago erupted or imploded. Left behind is the vast Caldera (volcanic crater) which is most apparent from the area known as Los Roques. Los Roques are a group of giant, flamboyantly shaped lumps of volcanic rock rising out of the crater; often visited and photographed.
68:Santa Cruz de la Palma
71:The Calle Real is a delightful street in which to stroll and enjoy the atmosphere. At its southern end it takes on the improbable title of Calle O’Daly, named after an Irish banana merchant who settled on the island. Look, also, on the parallel Avenida Maritimo at the wonderfully charming row of old houses known as the Casas de los Balcones Houses with balconies, built in the 19th century, they have become symbolic of Santa Cruz. Colorful and characteristic, and with a Portuguese influence, they have overhanging balconies, and those facing the sea were once used as lookout posts.
74:Heading west from Santa Cruz the first stop of interest is Las Nieves, a village built on the mountainside. The first indication of it is a roadside bar, followed by the 17th-century Santuario de Nuestra Señora de las Nieves (Sanctuary of Our Lady of the Snows). This holds the venerated 14th-century terracotta image of the Virgen de las Nieves, which relates to an ancient miracle when the Virgin appeared in Rome during August snow. Every five years the image is carried to Santa Cruz in a procession known as La Bajada de la Virgen (the Descent of the Virgin).
77:Heading back north towards Santa Cruz, a stop at the Cueva de Belmaco is in order. Here, you will find the Parque Arqueológico de Belmaco (Archaeological Site of Belmaco). The first stone engravings found in the Canary Islands were discovered here in the 18th century, and the ten natural cave dwellings, with their magnificent rock engravings, were the home to the Benahoritas — the ancient settlers of Benahoare, the original aboriginal name for La Palma.
79:This is really of little interest, and the roads often leave something to be desired. However, a trip up the eastern coast from Santa Cruz to just south of Barlovento isn’t too long, and the rather serpentine road runs through some pretty scenery. Make the first stop the miradores of Bartolomé and La Montaña, with the latter being a little higher and affording beautiful vistas along the coast in both directions. Head next for the seaside village of San Andrés and its natural swimming pools at Charco Azul (blue pool). A little inland from San Andrés and Sauces is the Bosque de Los Tilos, the largest wooded area in the whole Canary Islands and designated a “Biosphere Reserve” under the protection of UNESCO. Heritage of Mankind is the information center above the restaurant (open Monday–Friday 8am–3pm). The final destination though is a lovely, remote site just before Barlovento where, after a tortuously twisting journey down through banana plantations, you will reach the Piscinas Fajana; literally swimming pools built into the rocks and fed by the ocean waters that often crash into them. Showers and toilets are on hand, as is the pleasant La Gaviota (the Seagull), a restaurant/bar, and the views north of the cliffs falling straight into the ocean and being pounded by waves are breathtaking.`  

In this example, `grep -n` found all of the lines containing "Santa Cruz" and revealed the lines that they could be found on in the file. This is useful  if the user wants to find where in the file the word or phrase comes up. 

### Example 2
Input:  
`grep -n "Although Amsterdam" travel_guides/berlitz2/*`  
Output:  
`travel_guides/berlitz2/Amsterdam-WhereToGo.txt:114:Although Amsterdam is a city of 750,000 people, a ten-minute journey can transport you out into the countryside with fields as far as the eye can see. You don’t need a car to visit and explore the pretty towns; public buses provide a very comprehensive, easy, and cheap service.`  

In this case, it also prints out the line that the phrase "Although Amsterdam" can be found on. 
