###### range
| Name        | Symbol | Binary | Number of bytes                   | Equal to |
| :---:       | :---:  | :---:  | ---:                              | :---:    |
| `Kilobyte`  | KB     | 2 / 10 | 1,024                             | 1024 B   |
| `Megabyte`  | MB     | 2 / 20 | 1,048,576                         | 1024 KB  |
| `Gigabyte`  | GB     | 2 / 30 | 1,073,741,824                     | 1024 MB  |
| `Terabyte`  | TB     | 2 / 40 | 1,099,511,627,776                 | 1024 GB  |
| `Petabyte`  | PB     | 2 / 50 | 1,125,899,906,842,624             | 1024 TB  |
| `Exabyte`   | EB     | 2 / 60 | 1,152,921,504,606,846,976         | 1024 PB  |
| `Zettabyte` | ZB     | 2 / 70 | 1,180,591,620,717,411,303,424     | 1024 EB  |
| `Yottabyte` | YB     | 2 / 80 | 1,208,925,819,614,629,174,706,176 | 1024 ZB  |
  
```java
public class CommonConstant {

	private static final long BYTE = 1024;
	private static final long MEGABYTE = BYTE * 1024;
	private static final long GIGABYTE = MEGABYTE * 1024;
	private static final long TERABYTE = GIGABYTE * 1024;
	private static final long PETABYTE = TERABYTE * 1024;
	private static final long EXABYTE = PETABYTE * 1024;
	private static final long ZETTABYTE = EXABYTE * 1024;
	private static final long YOTTABYTE = ZETTABYTE * 1024;
}
```
