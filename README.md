# cooling-fan
A cooling fan dataset containing vibration patterns of various fans at silent and noisy environments
## Raw Data
Various vibration patterns are stored in `DATA/` directory. Below is meaning of the directory name.
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
- `12cm_hmlo`: 12cm fan at different speeds (h, m, l, and o)
- `14cm_h`: 14cm fan at 2000rpm
- `14cm_m`: 14cm fan at 1600rpm
- `14cm_l`: 14cm fan at 1200rpm
- `14cm_o`: 14cm fan at 0rpm
- `14cm_hmlo`: 14cm fan at different speeds (h, m, l, and o)

Below are types of fans.
- `normal`: normal fan
- `damage1`: unbalanced fan with holes
- `damage2`: unbalanced fan with a chipped blade

Below are environments.
- `silentA`: office room A
- `silentB`: office room B
- `noisy`: office room near a ventilation fan

Each directory contains a series of frequency spectrums ranging from 1Hz to 512Hz at 1Hz resolution. A single frequency spectrum is stored in CSV file. In `h`, `m`, `l`, and `o` patterns each contains 300 CSV files at a constant speed. In `hmlo` patterns each contains 235 CSV files in which the speed is changed in the order of h, m, l, and o. An animated frequency spectrum in MP4 format is also provided for each directory.

## Example Tasks
Below are examples of machine learning tasks using this dataset.

| Task name | Train data | Test data | Description |
| ---- | ---- | ---- | ---- |
| 2500rpm | 12cm_h_normal_{silent,noisy} | 12cm_hmlo_normal_{silent,noisy} | To detect different fan speeds other than 2500rpm at a given environment |
| 2000rpm | 12cm_m_normal_{silent,noisy} | 12cm_hmlo_normal_{silent,noisy} | To detect different fan speeds other than 2000rpm at a given environment |
| 1500rpm | 12cm_l_normal_{silent,noisy} | 12cm_hmlo_normal_{silent,noisy} | To detect different fan speeds other than 1500rpm at a given environment |
| 0rpm    | 12cm_o_normal_{silent,noisy} | 12cm_hmlo_normal_{silent,noisy} | To detect different fan speeds other than 0rpm at a given environment |
| damage1 | 12cm_\*_normal_{silent,noisy} | 12cm_\*_damage1_{silent,noisy} | To detect damaged fan at a given environment |
| damage2 | 12cm_\*_normal_{silent,noisy} | 12cm_\*_damage2_{silent,noisy} | To detect damaged fan at a given environment |
| 4speed | 12cm_hmlo_normal_{silent,noisy} | 12cm_hmlo_normal_{silent,noisy} | To classify four speeds at a given environment |

## Reference
You can find more information about this dataset in the following preprint. If you use this dataset, please cite it in your paper.
> Hiroki Matsutani, Mineto Tsukada, Masaaki Kondo, "On-Device Learning: A Neural Network Based Field-Trainable Edge AI", 	arXiv:\*\*\*\*.\*\*\*\*\*, March 2022.
