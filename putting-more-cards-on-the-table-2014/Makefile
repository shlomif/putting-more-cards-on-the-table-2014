all: test output

test:
	xmllint --noout --relaxng ./extradata/fortune-xml.rng source.xml

output: out.xhtml

XSLT_SS = extradata/fortune-xml-to-html.xslt
out.xhtml: source.xml $(XSLT_SS)
	xsltproc --output $@ $(XSLT_SS) $<
