# vsdiat_pd
Physical Verification by Sky130 PDKs

Mentorship: Kunal Ghosh
Instructor: Tim Edwards
(Focused on DRC/LVS using opensource technology Skywater 130nm)


# Day1: 

Using Google Skywater 130 PDK: Digital Standard cells, Primitives, I/O cells.

> Clone the repository git clone https://github.com/RTimothyEdwards/open_pdks ; 
Run cd open_pdks ; 
Run ./configure --enable-sky130-pdk ; 
Run make ; 
Run sudo make install .

However, workshop and following activites are carried in cloud-based environment.

Various Tools: Magic(Layout), Xschem(Schematic), Netgen(LVS), Ngspice(Analog Simulation)

Project Structure:
Project----> xschem/xschemrc
             ngspice/spinit
             mag/magicrc
             netgen/tcl


*Inverter*

## 1. Opening xschem


![image](https://user-images.githubusercontent.com/36757243/195299034-6559a827-a001-465b-99f5-297073f0a62f.png)
Default screen
![image](https://user-images.githubusercontent.com/36757243/195299810-3e6cd0c9-b8e2-4737-a7ef-fccf5b6915c2.png)

Helpful resource: https://xschem.sourceforge.io/stefan/xschem_man/xschem_man.html


## 2. Opening magic
![image](https://user-images.githubusercontent.com/36757243/195300902-db866275-5871-4239-a4fe-4ac80def45cb.png)
Basic scren
![image](https://user-images.githubusercontent.com/36757243/195301035-ec60c19a-8351-447b-be1b-b6220f14c6c2.png)

![image](https://user-images.githubusercontent.com/36757243/195301152-e8efdec6-8f89-4110-859c-b430c8156c23.png)

Helpful resource: http://opencircuitdesign.com/magic/tutorials/


## 3. Making devices and params 
![image](https://user-images.githubusercontent.com/36757243/195306318-7d84dd5e-fcce-4ed8-a30e-1b45c0a5d972.png)

![image](https://user-images.githubusercontent.com/36757243/195306661-51edb10d-226b-4a9d-81ca-c6cb079ef4e7.png)



## 4. Inverter schematic
![image](https://user-images.githubusercontent.com/36757243/195315676-dba759ca-232d-4f17-ad8f-2bc6cadbe13f.png)

NFET
L=0.18
W=4.5
nf=3

PFET
L=0.18
W=3
nf=3

## 5.Creating symbol to test with interfacing for test bench

![image](https://user-images.githubusercontent.com/36757243/195323911-6d523996-ca63-4e77-9d1f-7c284edcd5f6.png)

Symbol powered with PWL(0,0,20n,0,900n,1.8) and vdd 1.8
Simulation corner: "tt"


![image](https://user-images.githubusercontent.com/36757243/195360404-c086a4b2-e19a-4cbf-a6ab-7611d1a72cb4.png)

## 6.Simulation:
netlist
![image](https://user-images.githubusercontent.com/36757243/195360510-58951571-d392-42b0-b05a-1da2f582af2b.png)
![image](https://user-images.githubusercontent.com/36757243/195361916-dd9780f1-b879-419b-8329-7222476291c1.png)
![image](https://user-images.githubusercontent.com/36757243/195361986-1cfcd7e2-48cc-434c-b105-9e067a233658.png)

However, due to certain mismatch simulation results I was unable to reach simulation results.


## 7. Layout

![image](https://user-images.githubusercontent.com/36757243/195389371-83a615e4-dee0-41b1-b9c3-9f1db59ddb3f.png)


Writing files from magic to local dir
![image](https://user-images.githubusercontent.com/36757243/195565431-b8dfc974-4de5-4c0d-9787-02567e059216.png)
![image](https://user-images.githubusercontent.com/36757243/195565803-a4f06b62-7f2c-4c08-bfb8-dd91ba1cd770.png)


## 8. LVS



