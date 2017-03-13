
Microhousing is an alternative, and counter-movement to the ever growing sizes of personal and family housing.

Activities
----------

That a house should accommodate.

* Sleeping
* Leisure
* Working
* Socializing
* Cooking
* Meta: Improving the house

Design for actual use. Currently in central Oslo apartment, I

* Spend most of my time at desk, in front of computer and 3d-printer.
* Sleep once a day ~8 hours, most days alone.
* Cook upward of 1 (hot) meal a day. Rest is bread+spread, cereal etc.
* Most meals doable with just 2 pots. Oven optional.
* I shower usually once a day. Spend less than 45 mins total in bathroom.
* I occationally have visitors, usually one, sometimes two.

Needs
------

* Bed, double sized.
* Guest sleeping surface.
* Good sized working surface / desk.
* Bathroom: Shower, toilet, sink
* Kitchen: Oven+stovetop, fridge+freezer, sink

Wants
------

* House to be transportable, for instance mounted on trolley
* Window looking out from working area
* Window looking out from sleeping area

Esthetics
--------

* Minimal
* Functional
* Post-modern?
* Tech meets nature

Ideas
------

Dual/multi-purpose areas

* Functions which are not needed/utilized at the same time should be able to serve multiple purposes
* Should to take into account more than 1 person using the space. Could be 2 typically, 3 people occationally.
* Maybe integrate shower with toilet+sink into one cabinet that is "bathroom". Use water-tight compartments to keep toiletries+towel while showering.

Roof balcony

* Multiplies available space
* Can be used for storage, of bicycle/skis for instance.
* Can be used to plant/grow things
* Washing machine, and drying clothes
* Social space when more than a couple of people
* Challenge: Keeping water/snow from destroying roof, need good drainage.
* Let balcony be sparse floor, mounted on top of slanted roof?

Research topics
--------------

* Housing regulations in Norway, Scandiavia and EU.
* Regulations for trolley size etc. B1: ~750-1250kg, BE: 3500kg.
* Possible locations to keep a microhouse. Camping?
* Contruction methods

Documentation
--------------

* Each solution should be documented well enough to be usable stand alone
* Include rationale, constraints and inspirations

Subsystems
-----------

Electricity

* Budget: 200 watts average, with non-electic heating
* Regular: Computer/phone, work/reading lights.

CleanWater

* Capture rainwater?
* Storage needed. Many use 300-400 liters. Tanks can hopefully go outside.
* waterHavested (liter) = roofArea (m2) * rainfall (mm) * 0.8 (collection factor). 25mm/30days @ 15m2 = 10 l/daily. Minimum?

Hotwater

* For showering, cleaning dishes
* The average American shower uses 65.1 liters of water and lasts for 8.2 minutes at average flow rate of 7.9 liters/minute.
* Should have grey-water heat-exchanger for shower. More beneficial the colder the input water is.
* Per person 50 liters/daily hotwater. 2.5kW/daily. http://www.esru.strath.ac.uk/EandE/Web_sites/09-10/Hybrid_systems/solar-thermal.htm
* 2 m2 flat-bed indirect active panel should be able to provide this.
* Seems to be available as kit for ~1000EUR. http://www.ecosolarspain.com/untitled-sitepage_10
* Solar water (pre)heating doable in warmer climates
* Nice list of 1k USD DIY heaters, http://www.builditsolar.com/Projects/WaterHeating/water_heating.htm#1KSolarWater
* North/mid-Spain has average annual solar irridiation in excess of 1500 kWh/m2/year, or 4 kWh/m2/day.
http://www.builditsolar.com/References/Measurements/CollectorPerformance.htm#Efficiency
* Hot water good way to store surplus energy
* Normal also need an on-demand heating solution. Electric/gas/oil/wood
* Heating on stove

Solar water heater

Panel, 60x100cm

* Glazing. 10-13 EUR. http://www.mwmaterialsworld.com/es/materiales/metacrilato-y-policarbonato/policarbonato-celular/plancha-de-policarbonato-celular.html
http://www.leroymerlin.es/fp/10603033/placa-policarbonato-celular-sedpa-
http://www.leroymerlin.es/fp/10784221/placa-policarbonato-celular-sedpa-
* Collector: 13 EUR PC channels, 25++ EUR alu plate, 50++ EUR copper.
http://www.mwmaterialsworld.com/es/materiales/metal/cobre/plancha-de-cobre-industrial.html
http://www.aki.es/productos/chapa-aluminio-bruto-liso/idp18745
http://www.aki.es/productos/chapa-aluminio-anodizado-ondulado/idp18792
* Tubing. 10 EUR
* Paint. Absorbtion, protective. 10 EUR.
* Insulation. 10 EUR
* Framing. 10 EUR.

Total, 70-120. For ~2m2 need 3 such panels, 300 EUR.

* Pump: 50 EUR. Also needs electricity. Alternative, thermosiphing.
* Tank: 100 EUR. Might be part of general hotwater system
* Heat exchanger. 50 EUR for simple copper-tubing in tank type.
https://www.garciaruiz.es/webcms/index.php?menu=tiendavirtual&submenu=ficha_producto&id_producto=881&gclid=CNrMhNudjNICFUmNGwodONwE5Q
Single-wall, so requires use of non-toxic fluid in solar-cell loop, such as Propylene Glycol.
* Heater fluid additives. 25+ EUR.
http://www.ebay.es/itm/5-LITRES-Propylene-Glycol-PG-USP-EP-GRADE-/281053133185
https://www.amazon.com/Propylene-Glycol-Perfect-Sweetness-Highest/dp/B00GI2CIQS

Smarts

* Flow sensors.
https://www.adafruit.com/product/828 / http://www.dx.com/p/yf-s201-hall-effect-water-flow-counter-sensor-black-217625
Feedback-based system. Attempt to hit a certain flow rate. Measure/check the needed voltage (PWM dutycycle) to get there.
This can then be tracked over time, indicating the 'resistance' in the system.
If exceeding certain threshold, give warning.
One can also swap the water in the system a known volume) periodically instead of running continiously. Can help the pump.
* Temperature sensors.
http://www.dx.com/p/waterproof-ds18b20-temperature-sensor-with-adapter-module-for-arduino-429959

Would be nice to have temp in+out, and flow per panel.

Questions

* How much water should be inside the collector?. This dictates size of channels.
* Can we use alu sheet for collector combined with copper tubing in heat exchanger? Do we need sacrifical anodes?
* Can we avoid the fairly expensive metal sheet if the surface area is large enough? How much does it impact effectivity
* If using transparent plastic as collector, should probably paint backside black. The portable plastic bag heaters do this.
* Can we use corrugated aluminium roofing sheets as front for collector?
Available at 25 EUR/m2, but maybe only in large sizes.[1](https://www.maxbo.no/takplate-20-105-sort-hc25-2-5m-plannja-p20-dekkbredde-1050-svart-t-0-50mm-p447375). Non-alu:
[2](http://www.leroymerlin.es/fp/18211200/cobertura-metalica-ondulada-sedpa-?idCatPadre=600369&pathFamilaFicha=381201)
[3](http://www.leroymerlin.es/fp/10020752/cobertura-metalica-ondulada-sedpa-?idCatPadre=600369&pathFamilaFicha=381201)
However, very useful in general when making a house, both for roofing and possibly for walls.
Challenge is plumbing the corrugated shape at top/bottom.
Welding alu/alu is ideal, but speciality skill+tools.
Can we just silicone the shit to a flat with drilled holes in them?
* Tank temperature must be minimum of 49 degrees, to prevent Legionaires bacteria. 60 degrees is recommended (by WHO).
At 60 plus degrees they die very fast, so daily spikes above to this may be good.
49 degrees max at tap is recommended to protect against scolding.

Other uses

* Public showers.
* Showers for events, like festivals etc
* Use for water purification. Both the heat and UV radiation contributes.
[Solar water disinfection](https://en.wikipedia.org/wiki/Solar_water_disinfection).
Note: Polycarbonate (resin identification code 7) blocks all UVA and UVB rays.

Tools

* Solar power meter. "Pyranometer". For measuring the irridiance of the sun. Watt/m2 or Btu
https://www.amazon.com/Dr-Meter-SM206-Digital-Solar-Power/dp/B008R5W2J2

Refs

* http://www.builditsolar.com/Experimental/CopperAlumCollector/Performance.htm

Water purification

* [Turbidity](https://en.wikipedia.org/wiki/Turbidity) is a key measurement of how much (small) particles are in the water,
measured optically. WHO says turbidity of drinking water should not be more than 5 NTU, and should ideally be below 1 NTU.
There is an open-source design of a hand-held unit in the [wash4all project](https://github.com/wash4all/open-turbidimeter-project).
Another design at [Appropedia: Water quality testing platform](http://www.appropedia.org/Open-source_mobile_water_quality_testing_platform)


Solar electricity

* Seems like cells can be had for 500 EUR/kW.
* 12 volt batteries at 150 EUR / 100 Ah.
* A 1kW system with 2kWh storage might be doable for 1000 EUR in parts, including charging and inverter.

Heating

* Depends a lot on climate..
* Source. Wood? Gas? Electric?
* Distribution. Airflow. Waterbourne?
* Water can make use of solar thermal

Cooling/ventilation

* Only needed in warm climates. Like Spain 2-3 months in summer
* https://en.wikipedia.org/wiki/Solar_chimney

Cooking

* Power source. Wood? Gas? Electricity is off if to be off-grid capable.

Storage

* Clothing
* Bicycle
* 

Location
----------

Common

* Not needing a car. Public transportation access to city/airport. Biking/walking distance to grocery store.
* Ease of travelling to Norway/EU
* + Opportunities to swim and bike/hike nearby

Oslo-ish, Norway

* - Cold in winter
* - Expensive plots
* + Known language
* + Secure/stable environment

Balkans

* Croatia/Serbia/Montenegro
* Should be close to sea, walking distance.
* + Temperate climate
* + Cheap-ish plots
* Maybe ability to rent out in season. Croatian tourism regulations quite strict however
* Plot listings [Montenegro](http://www.montenegroprospects.com/property/page/9/?st=property&s&t_region=--&t_property_type=--&price_from=--&price_to=50000)
* Agricultural land over 3300sqm in Croatia can build house on
* Islands of Brac, Hvar, Korcula, Vis all have ferry/boat connection to Split center. Plots `< 20000EUR`
* (smaller) islands Otto Sipan, Lopud and Kolocep are connected to Dubrovnik.
* Connections to islands outside Pula/Rijeka (Cres/Losinj) seems less developed

Croatia, islands around Split

* [Solta](http://www.realestatecroatia.com/eng/list.asp?mjesto=%C5%A0OLTA&sort=cijena&smjer=asc&submit=%3E%3E)
* [Hvar](http://hvar-properties.com/search-results/search&category=&cijena-from=0&cijena-to=50000/)
* Brac
[1](http://www.broker.hr/Search/All/None/Brac/status3/)
[2](http://www.realestatecroatia.com/eng/list.asp?mjesto=BRA%C4%8C&sort=cijena&smjer=asc&submit=%3E%3E)
* Split-Dalmastiska
[houses](http://www.realestatecroatia.com/eng/list.asp?vrsta=1&akcija=1&regija=17&opcina=..&cijena=Between+10000+And+35000&valuta=EUR&povrsinaOd=&povrsinaDo=&sort=cijena&smjer=asc&pagesize=40&foto=1&Submit=+)
[land](http://www.realestatecroatia.com/eng/list.asp?vrsta=3&akcija=1&regija=17&cijena=Between+10000+And+35000&valuta=EUR&povrsinaOd=&povrsinaDo=&sort=cijena&smjer=asc&pagesize=40&foto=1&Submit=+)

Croatia, cities around Split

* Omis
* Marina
* Kastela

Note: Camping outside dedicated campites [is illegal](http://www.camping.hr/camping-croatia/faq)


Legalities Croatia

* Buy a house in Croatia, the key documents you need. http://www.liveistria.com/?p=2894
* Limitations on foreign purchases in EU. https://tranio.com/traniopedia/tips/european_limitations_on_foreign_property_purchases/
Croatia: Foreign citizens cannot buy agricultural land, unless they create or buy it through a Croatian company.
* "Starting from date 01.02.2009 the Croatian government has removed all of its restrictions"
http://www.adriatica-estate.com/buying-guide-property-in-croatia/en-755.html

References
-------------

Existing microhouses

* [(Norwegian) Matias og Sara 11kvm mikrohus på hjul](http://www.aftenposten.no/bolig_old/Huset-deres-kostet-100000-kroner-og-er-pa-11-kvm-7861757.html)
* Jakobs sauna-fleet
* [2.6m cube, 7sqm pre-fab microhouse, 2.2 tons](http://www.microcompacthome.com/)
* Kolonihagene i Oslo
* [Podhouse, prefab 6-12 sqm microhouse](http://podhouse.info/en/)
* [(Norwegian) Wooden concept micro-house](http://www.dinside.no/923143/her-skal-en-svensk-student-bo)
* [Bunkie, prefab 10 sqm Canadian](http://www.thebunkie.com/)
* [15 sqm house in New Zealand](http://www.treehugger.com/tiny-houses/living-big-in-a-tiny-house-tour-brett-sutherland-tiny-house.html)
[video](https://www.youtube.com/watch?v=VckbqU4kK2I). Smart movable toilet.

Container-based builds

* [Container Guesthouse](http://www.poteetarchitects.com/containerguesthouse/1.html)
* [Two-tree House](http://www.golanyarchitects.com/Golany%20Architects_Residence%20nr%20Jerusalem_01.htm). All-wooden exterior, built around two living trees. 
* [Port-a-Bach](http://www.atelierworkshop.com/port-a-bach). Sidewall folds down to form deck.
* [Platoon collective house (Berlin)](https://www.flickr.com/photos/angermann/2268782521/)
* [Echo Eco Pod](http://www.gizmag.com/echo-eco-pods/33617/pictures#33)
* [20' off-grid](https://www.youtube.com/watch?v=2l58L3QEVnc). Nice bedroom/louge split.

Hexayourt

* Geodesic structures built with minimal modifications on lightweight 4'x8' material, and fiberglass-reinforced tape for joining together.
* Design is in the public domain, with lots of documentations and variations.
* Appropexia: [Hexayurt](http://www.appropedia.org/Category:Hexayurt_project).
* Appropedia: [Hexayurt Playa](http://www.appropedia.org/Hexayurt_playa), specifically around building for Burning Man.
* [Personal blog of the Hexayurt creator](http://vinay.howtolivewiki.com/blog/)
* [EMF204: Hexayurt, Distributed Infrastructure, and Maximizing Global Minimalism](https://www.youtube.com/watch?v=dSD6DhuqFzA)
"|as an opensource community|, why don't have we done anything about housing?"
aligns the Napster->Spotify with situation of building codes.
vested interests in having housing be expensive: large profitably industry, expensive housing (incl utilities and mortage) is a basis for tax.
Goal of free software movement is to ensure freedom -> but we're still limited by physicals.
"we're (opensource) winning in software, making good inways in electronics, and gadgets. Need to move into basic physical infrastructure: housing, watersupply, energy".
What if we could have a 200-500 people nomadic village built of hackers, with open source infrastructure shipped around in containers.
* PIR plus. polyisocr. Brand names include: 
* EU sellers. http://www.srx400.co.uk/buyonline/buy/celotex 20 sheets of 40mm looks to be 360 GBP+shipping.
* Kingspan/SPU. http://www.spu-isolering.no/produkter/produkt/kingspan-therma-tr26-fr-spu-sp/ or http://www.spu-isolering.no/produkter/produkt/kingspan-therma-tp10-tf70-tw50-tw55-fr-spu-al
* https://hipro.no/ sells PIR-sandwich materials
* For living in semi-permanentlu, the tall hexayurt variations are probably the way to go. H15 (6 foot sidewalls) or H18 (8 foot sidewalls).


Watersystem

* [Hot water using stove and thermosiphoning](https://www.youtube.com/watch?v=5IRLVCJ1olA)

Solar water heaters

* Can be used
* [DIY solar water heating](http://www.reuk.co.uk/wordpress/heating/diy-solar-water-heating/), practical guide.
Covering basic principles, suggestions for build.
* [](http://www.reuk.co.uk/wordpress/solar/evacuated-tube-solar-water-heating/)

Heating

* Woodgas stoves. Use a secondary burn to achieve higher efficiency and cleaner burn.
http://www.woodgas-stove.com/ https://wildstoves.co.uk/product/wild-woodgas-stove-budget-duo-kit/

Bedding

* [Slide it under floor](http://www.treehugger.com/sustainable-product-design/living-with-less-first-hide-the-bed.html)

Online communities

* [mikrohusprat.no](http://www.mikrohusprat.com/) Norwegian micro-house forum

Practicing communities

* Global Ecovillages Network. [list of projects](http://gen.ecovillage.org/en/projects/459/all)
* [Cohousing](http://www.cohousing.org/what_is_cohousing)

Norwegian regulations

* [Regjeringen: On temporary buildings](https://www.regjeringen.no/no/dokumenter/-20-1-bokstav-j-og--20-2-bokstav-c---Tilbakemelding-pa-henvendelse-om-midlertidig-bygning-konstruksjon-eller-anlegg/id2008989/)
* [Jusstorget.no: Excemptions from building permits](https://www.jusstorget.no/byggeprosjekter-som-er-fritatt-fra-reglene-om-byggetillatelse/)

Politics

* [Housing without debt](https://medium.com/@AlastairParvin/housing-without-debt-5ae430b5606a) by WikiHouse Foundation co-founder.
Argues for building an alternative market for houses: as homes for people - not assets for speculation.
