PACKAGE := hello_1.0-1_amd64
DEPENDS := $(shell find $(PACKAGE) -type f)
TARGET := $(PACKAGE).deb

$(TARGET): $(DEPENDS)
	dpkg-deb --build --root-owner-group $(PACKAGE) $(TARGET)

all: $(TARGET)

.PHONY: clean
clean:
	rm -rf $(TARGET)