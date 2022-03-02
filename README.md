# cooling-fan
A cooling fan dataset containing vibration patterns of various fans at silent and noisy environments
## Overview
A series of vibration patterns is stored in each directory. Below is meaning of the directory name.
~~~
<size>_<speed>_<type>_<environment>
~~~
Below are size and speed pairs included in this dataset.
- `8cm_h`: 8cm fan at 4000rpm
- `8cm_m`: 8cm fan at 3600rpm
- `8cm_l`: 8cm fan at 3200rpm
- `8cm_o`: 8cm fan at 0rpm
- `8cm_hmlo`: 8cm fan at different speeds (h, m, l, and o)
- `12cm_h`: 12cm fan at 2500rpm
- `12cm_m`: 12cm fan at 2000rpm
- `12cm_l`: 12cm fan at 1500rpm
- `12cm_o`: 12cm fan at 0rpm
- `12cm_hmlo`: 8cm fan at different speeds (h, m, l, and o)
- `14cm_h`: 14cm fan at 2000rpm
- `14cm_m`: 14cm fan at 1600rpm
- `14cm_l`: 14cm fan at 1200rpm
- `14cm_o`: 14cm fan at 0rpm
- `14cm_hmlo`: 8cm fan at different speeds (h, m, l, and o)

Below are types of fans.
- `normal`: normal fan
- `damage1`: unbalanced fan with holes
- `damage2`: unbalanced fan with a chipped blade

Below are environments.
- `silentA`: office room A
- `silentB`: office room B
- `noisy`: office room near a ventilation fan

## Vibration Patterns
Each directory contains a series of frequency spectrums ranging from 1Hz to 512Hz at 1Hz resolution.
A single frequency spectrum is stored in CSV file. 
{h,m,l,o} datasets contain 300 CSV files, and hmlo datasets contain 235 CSV files.
An animated frquency spectrum in MP4 format is also provided for each directory.
