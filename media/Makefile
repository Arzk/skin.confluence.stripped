TARGET=Textures.xbt
XBMCTEX=/build/buildd/xbmc-11.0-pvr+yavdr3-pipelka-eden-git20120415.f57e18b/tools/TexturePacker/TexturePacker

IMAGES := $(shell find . -name "*jpg")
IMAGES += $(shell find . -name "*png")
IMAGES += $(shell find . -name "*gif")

all: $(TARGET)

.PHONY: force

$(TARGET): $(XBMCTEX) $(IMAGES)
	$(XBMCTEX) -input . -output $(TARGET)

$(XBMCTEX): force
	$(MAKE) -C /build/buildd/xbmc-11.0-pvr+yavdr3-pipelka-eden-git20120415.f57e18b/tools/TexturePacker

clean:
	rm -f $(TARGET)
distclean: clean

