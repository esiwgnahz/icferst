input:	clean
	./copy_script
	gmsh -2 -bin src/MMS_A.geo
	gmsh -2 -bin src/MMS_B.geo
	gmsh -2 -bin src/MMS_C.geo
	gmsh -2 -bin src/MMS_D.geo

clean:
	rm -f *.vtu *.stat *.s *.log *_A* *_B* *_C* *_D* src/*A.* src/*B.* src/*C.* src/*D.* matrix* *~ mms_p1dgp2_stressform_rb_sp.py *.pyc fluidity.*
