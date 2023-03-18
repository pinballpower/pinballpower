# Mrgin multiple scans

```
FILES="SCAN0022.TIF SCAN0023.TIF"
pto_gen -p 2 -f 1 -o project.pto $FILES
cpfind -o project.pto --celeste project.pto
pto_var --opt TrX,TrY,TrZ,Tpy,Tpp -o project.pto project.pto
autooptimiser -p project.pto -o project.pto
pano_modify -o project.pto --center --straighten --canvas=AUTO --crop=AUTO project.pto
nona -v -m TIFF_m -o project project.pto
```
