markdown_srcs := $(wildcard *.md)
markdown_web   = $(markdown_srcs:.md=.html)
markdown_pres  = $(markdown_srcs:.md=_pres.html)

all : $(markdown_web) $(markdown_pres)

%.html : %.md
	markdown -x def_list -x codehilite -f $@ $<
%_pres.html : %.md
	landslide -l no -x def_list $< -c -r -d $@

clean: 
	rm -rf theme *.html *~