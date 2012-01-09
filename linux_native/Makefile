# Allgemeines geheule
# * WÄÄÄH Warum ist Foundation und CoreFoundation so durcheinander?
# * objc-c++ Zeux geht (noch) nicht → in gcc-runtime nicht fertig und aus coco-runtime nicht
#									extrahiert (wahrscheinlich auch von Compiler-Patches abhängig)
# * object_msgSendv ((old) GCC api objc_msg_sendv) geht nicht → Spezialcode und keine
#																runtime-Entsprechung?
#																(Spezialcode in Foundation nicht rt)


PROJECTS = test Foundation


.PHONY: all
all: $(PROJECTS)


.PHONY: $(PROJECTS)
$(PROJECTS):
	@$(MAKE) -C $@

test: Foundation

.PHONY: clean
clean:
	@$(foreach project,$(PROJECTS),$(MAKE) -C $(project) clean;)
