NAME=proj1.
LOGIN=xsyano00

all:
latex $(NAME)tex
dvips -t a4 $(NAME)dvi
ps2pdf $(NAME)ps
zip:
zip $(LOGIN)-fit.zip *.tex Makefile
clean:
rm -f $(NAME){out,aux,dvi,log,ps,pdf}
