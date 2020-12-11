# uniDelta
Parametric and scalable design of a delta 3d-printer frame.

# Preview
See on autodesk site.
https://a360.co/3fAnUOM

# Description
Key features, I made this design around:
+ be suitable for any size of a delta printer
+ use of aluminum extrusion and basic accessories
+ be suitable for V-slot sliders or linear rails
+ easy to enclose
+ be easily customizable for any size
+ cheap

Project is designed in Fusion 360.

# How to use this model
Use .f3z file to import it into Fusion 360.
Make sure "geometry_ref" sketch is visible. Make sure dimentions on the sketch are shown. If not, right click on sketch in browser -> Show Dimentions.
Then check model parameters in "Modify > Change Parameters" menu. Here you can find parameters, that make this design universal.
- *bed_diameter* -> Set it to a diameter of your working space. Usually, you want it to coincide with a dimeter of your printing bed.
- *bed_to_stand_offset* -> This is a distance from bed edge to a vertical stand. You should consider a number of factors, when assigning this parameter.
  - Size of your effector. There sould be enough offset to a nozzle to being able to reach a bed edge.
  - Mount points of printer arms on a slider carriage. Arms should not go any further than a vertical position, when a nozzle reaches an edge of working space.
  - Keep bed inside a frame perimeter, if you want to make a printer enclosed. If not, it is not crucial
- *height* -> Overall height of a frame.
- *T_stand* -> Vertical stands design is based on goeland86/MonsterKossel. So vertical stands are made of one 2040and one 2060 rods slaped together for super rigidity for bigger frames. If you want a small one or cut a budget, set *T_stand* to 0. Then make now unused 2060 invisible. Set *T_stand* to anything other than 1 or 0 to see various bugs.
Now about sad things. Fusion 360 is limited in a way how parameters are calculated. So, for now, you are not able to make a driven dimention on a scketch a paraeter. That leaves two options. Either I have to analitically solve all the geometry (and I do not have courage for that) or some parameters have to be manually transferred from *geometry_ref* sketch to a parameters menu. I choose a latter option. So, please, refer to *geometry_ref* sketch and enter following parameters.
- *side_extrusion* -> The length of side extrusions on bottom and top, that forms rings around vertical stands. Enter a corresponding number from *geometry_ref* sketch. If you do not cut extrusions yourself, usually it comes cut to a 1mm precision (like from soberyzavod.ru). So you want to adjust *bed_to_stand_offset* untill it yelds in a nice round side_extrusion length. It will help you to keep a geometry tight at an assembly process.
- *inner_extrusion* -> The lentght of inner pieces of extrusion. Enter a corresponding number from *geometry_ref* sketch.

# Options and modifications
- you can change *T_stand* parameter to use only 2040 extrusion as vertical stands
- ring of 2020 extrusions on the bottom are optional. If you will choose not use them I recommend to fasten 2040 ring with not one, but two L-brakets to each vertical stand
- I would recommend to use OpenBuilds type of L-brakets to fasten bottom ring to vertical stands (6 pcs.) because of their strict 10x10x10 dimensions and 90 deg. edges. It will keep geometry strict. However, you can get away with using any type of plates and brackets in other connections. Get cheap ones or 3d-print them.
- Archie delta robot compatible design. https://www.thingiverse.com/thing:3489886
- I advise to use v-slot for vertical 2040. Then it will be compatible with v-slot carriage in case of modification or selling.

*_If you don't have ability to use Fusion 360, please, feel free to request design needed via "Issues". I will try ti generate .step for you._*

# Bill of materials
## 300x800mm kossel delta frame
### Aluminum extrusion
- [2020](https://www.soberizavod.ru/catalog/seriya_20_obychnyy_paz/profil_konstruktsionnyy_20kh20l_bez_pokrytiya/)
  - 398mm **x6**
  - 168mm **x3**
  - 136mm **x1**
  - 134mm **x6**
- [2040](https://www.soberizavod.ru/catalog/seriya_20_obychnyy_paz/profil_konstruktsionnyy_20kh40l_bez_pokrytiya/)
  - 398mm **x3**
  - 168mm **x3**
  - 134mm **x3**
  - 800mm ([v-slot](https://www.soberizavod.ru/catalog/seriya_20_v_paz/profil_konstruktsionnyy_v20kh40l_bez_pokrytiya/)) x3
- [2060](https://www.soberizavod.ru/catalog/seriya_20_obychnyy_paz/profil_konstruktsionnyy_20kh60l_bez_pokrytiya/)
  - 800mm **x3**
- [Tools to control angles](https://aliexpress.com/item/4000784066824.html)
### Plates and brackets
- [60 degree plate](https://www.soberizavod.ru/catalog/pod_uglom_seriya_20/u_soedinitel_60_gradusov_4_otv_paz_6_l57/) **x30**
- [Openbuilds L-type 3-slot](https://aliexpress.com/item/32843660148.html) **x6**
- [L-type bracket 3-slot](https://www.soberizavod.ru/catalog/uglovye_soediniteli_seriya_20/ugolok_20kh60l_paz_6_m52/) **x3**
- [L-type btacket 1-slot](https://www.soberizavod.ru/catalog/uglovye_soediniteli_seriya_20/ugolok_20kh20l_paz_6_m51/) **x12**
- [L-type plate](https://www.soberizavod.ru/catalog/g_obraznye_seriya_20/g_soedinitel_40kh60v_paz_6_l60/) **x2**
- [T-type plate](https://www.soberizavod.ru/catalog/t_obraznye_seriya_20/t_soedinitel_40kh50v_paz_6_l69/) **x1**
- [2-slot plate](https://www.soberizavod.ru/catalog/pryamougolnye_seriya_20/soedinitel_20kh40_paz_6_m45/) **x2**
- [motor plate](https://aliexpress.com/item/32813261164.html) **x3**
- [4040 plate (to move motors closer to stands)](https://www.soberizavod.ru/catalog/pryamougolnye_seriya_20/soedinitel_40kh40_paz_6_m48/) **x3**
### Kinematics
- [MGN12H with rail](https://aliexpress.com/item/32787326334) 500mm **x3**
- GT2 Gates timing belt **5 meters**
- GT2 Gates timing belt (for flying extruder lift, take cheapest)  **2 meters**
- M5x55 bolts (for top idlers) **x3**
- M5x30 bolts (for flying extruder lift) **x2**
- [Rubber band 4mm](https://aliexpress.com/item/32882540825.html) **4 meters**
- GT2 20t Pulley 5mm bore **x3**
- GT2 20t Idler Pulley 5mm bore **x3**
- Arms **x6**
  - [Magballs](https://duet3d.com/BallStudEnds) **x12**
  - Carbon fiber tubes, 318mm (5mm Inner Diameter) or (2mmID to use without M3 inserts, not recommended) **x12**
  - [Cup magnets B16](https://aliexpress.com/item/32966899291.html) **x12**
  - [M3 inserts (for 5mm ID carbon tube)](https://aliexpress.com/item/32811461060.html) **x12**
- Fastners
  - [M5x8](https://aliexpress.com/item/32811776016.html) **x300**
  - M5x12 **x6**
  - [M3 assorted](https://aliexpress.com/item/32831757502.html) **x1**
  - [M3x8](https://aliexpress.com/item/32769412937) **x30**
  - [M5 alum washers openbuilds 6.35mm](https://aliexpress.com/item/32753534988.html) **x18**
  - [M5 t-nuts](https://aliexpress.com/item/32706324351.html) **x300**
  - M3 t-nuts **x50**
  - M3 and M5 regular nuts and washers
  
# TODO
- Building instructions.
