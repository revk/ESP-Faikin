# PCB makefile (3d Cases)

%.stl:	%.scad
	echo "Making $@"
	/Applications/OpenSCAD.app/Contents/MacOS/OpenSCAD $< -o $@
	echo "Made $@"

stl: 	Faikin/Faikin.stl

Faikin/Faikin.scad: Faikin/Faikin.kicad_pcb PCBCase/case Makefile PCBCase/case Makefile
	PCBCase/case -o $@ $< --edge=2 --top=4.6 --bottom=2.6 --pcb=2

PCBCase/case: PCBCase/case.c
	make -C PCBCase
