[[_TOC_]]
## Additive Manufacturing 

### What is Shore Hardness?

---

[Shore hardness](https://www.smooth-on.com/page/durometer-shore-hardness-scale/) scales provide a point of reference when measuring the ***hardness*** of materials. 

![Shore Hardness chart](Images/durometer_chart.PNG)<div align="center">Figure 1: *Shore Hardness chart that delineates hardness of ubiquitous items*</div>

### Why use Thermoplastic Polyurethane (TPU) instead of Silicone?

---

"Typical" soft robots utilise [Silicone](https://www.smooth-on.com/products/ecoflex-00-30/) of eclectic Shore Hardness' to impart compliance. One of the critical requirements in this project was the speed of prototyping. This is where Additive Manufacturing (3D Printing) using TPU excels. TPU offers elasticity and flexibility whilst maintaining robustness.  

#### A few challenges that arise when using Silicone:

- Silicone takes a considerable amount of time to cure ([4](https://www.smooth-on.com/products/ecoflex-00-30/) hours - [16](https://www.smooth-on.com/products/dragon-skin-30/) hours). 
- Necessity of additional expensive equipment
    - Vacuum chamber and pump to remove air bubbles.
    - Inverse moulds of the end product are required to pour Silicone in them.
    - Weighing scales, gloves, eye protection gear, an apron and non-lather soap are necessary. 
- Accurate mixing ratio of Part A and Part B followed by slow stirring of the liquid rubber.
- A release agent spray for "easy" removal of the part from the mould.

### 3D Printing using TPU filament

---

#### Hardware requirements 

1. Use a **Direct drive extruder** (DDE): 
    - TPU filaments with a shore hardness in the range of **75A-85A** are physically like rubber bands in layman's terms. 
    - By using a DDE, one is guiding the filament straight down into the nozzle.
    - _Caveat_: TPU **95A** is flexible yet rigid enough to be used by an FFF printer (Ultimaker S5) with a **Bowden tube extruder**. 
    - [Direct drive v/s Bowden tube](https://www.3djake.com/info/guide/direct-drive-extruder-vs-bowden-extruder) 
2. TPU is **hygroscopic**:
    - TPU needs to be dry to obtain [successful prints](https://www.printables.com/model/339968-wet-filament-in-comparison-to-dry-filament-tpu-fle). 
    - Store filament in a Mylar bag filled with silica. 
    - Invest or make a [filament drying box](https://www.amazon.com/SUNLU-Filament-Filadryer-Compatible-Filaments/dp/B0B4WKQR24)

#### Slicer Settings 

|Parameter                  |Value          |Advice                                         | 
|:---:                      |:---:          |:---                                           |
|Print speed $(mm/sec)$     | $15 - 25$     |The slower the better. Unless you have a [Hemera](https://e3d-online.com/pages/hemera-feature-page)|
|Flow rate (%)              | $106 - 110$   |Incrementally adjust based on quality of print.|
|Infill (%)                 | $10 - 15$     |Adjust based flexibility of final product.|
|Infill Pattern             | Gyroid / Cross 3D    |If final product needs to be **flexible**.|
|Infill Pattern             | Cubic Subdivision / Grid    |If final product needs to be **rigid**.|
|Retraction distance ($mm$) | 8    |Lower the retraction distance if filament is getting stuck within the gears (75A is prone to this problem.)|

### Vendor list TPU (as of 2 Jan. 2022)

--- 

:heavy_check_mark: = Easy to print. Can use the material profile from this repo as a boilerplate. 

:warning: = Difficult to print

|Difficulty          | Filament Name  | Shore Hardness | 
|:---:               | :---:          | :---:          |     
| :heavy_check_mark: | [NinjaFlex](https://ninjatek.com/shop/ninjaflex/)      | 85A            |     
| :heavy_check_mark: | [Ultimaker-TPU](https://www.matterhackers.com/store/l/ultimaker-tpu-filament/sk/M5ZFDTT3)      | 95A            |    
| :warning:| [Chinchilla](https://ninjatek.com/shop/chinchilla/)      | 75A            |     