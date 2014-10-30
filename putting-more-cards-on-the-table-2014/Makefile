all: output

XHTML = putting-more-cards-on-the-table-2014
XHTML_MAIN = $(XHTML)/index.html

output: $(XHTML_MAIN)

$(XHTML_MAIN): source.db5.xml
	docmake -v \
	--stringparam "docmake.output.format=xhtml" \
	--stringparam "docmake.output.path_to_root=../../" \
	--stringparam "docmake.output.work_in_progress=1" \
	-x lib/sgml/shlomif-docbook/xsl-5-stylesheets/shlomif-essays-5-xhtml.xsl -o "$(XHTML)" xhtml-1_1 $<
