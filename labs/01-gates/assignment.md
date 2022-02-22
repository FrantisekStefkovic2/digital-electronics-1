zmena 
# Lab 1: Frantisek Stefkovic

### De Morgan's laws

1. Equations of all three versions of logic function f(c,b,a):
   ![IMG_20220222_165847](https://user-images.githubusercontent.com/99807711/155172966-bf7c82f6-9c18-42b5-918b-600d28e87f3a.jpg)
   ![IMG20220222164956](https://user-images.githubusercontent.com/99807711/155172996-b7179dc1-f730-439d-a09d-88a6244670d2.jpg) 
   ![image](https://user-images.githubusercontent.com/99807711/155175766-ca27b94a-ebeb-4e27-8bb5-dc36a812ac9b.png)

2. Listing of VHDL architecture from design file (`design.vhd`) for all three functions. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture dataflow of demorgan is
begin
    f_org_o  <= (not(b_i) and a_i) or (not(c_i) and not(b_i));
    f_nand_o <= (  (not(b_i) nand a_i) nand ( (not(b_i)) nand (not(c_i)))  );
    f_nor_o  <= not ( (not(a_i) nor b_i) nor (b_i nor c_i) ) ;
end architecture dataflow;
```

3. Complete table with logic functions' values:

| **c** | **b** |**a** | **f(c,b,a)_ORG** | **f(c,b,a)_NAND** | **f(c,b,a)_NOR** |
| :-: | :-: | :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 1 | 1 | 1 |
| 0 | 0 | 1 | 1 | 1 | 1 |
| 0 | 1 | 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 | 0 | 0 |
| 1 | 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 | 1 | 1 |
| 1 | 1 | 0 | 0 | 0 | 0 |
| 1 | 1 | 1 | 0 | 0 | 0 |

### Distributive laws

1. Screenshot with simulated time waveforms. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   ![image](https://user-images.githubusercontent.com/99807711/155171719-8abc9018-f3c2-4c7f-8f27-ae6c97778d7b.png)


2. Link to your public EDA Playground example:
   https://www.edaplayground.com/x/5L92
