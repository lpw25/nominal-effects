
OTTFLAGS=-tex_show_meta false -signal_parse_errors true -tex_wrap false

all : nominal-effects.pdf

nominal-effects-gen.tex : nominal-effects.ott
	ott ${OTTFLAGS} -i nominal-effects.ott -o nominal-effects-gen.tex

nominal-effects.pdf : nominal-effects.tex nominal-effects-gen.tex
	latexmk -pdf -pdflatex="pdflatex -interaction=nonstopmode" -use-make nominal-effects.tex

clean:
	latexmk -CA
	rm nominal-effects-gen.tex
