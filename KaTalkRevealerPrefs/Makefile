ARCHS := armv7 armv7s arm64 arm64e
TARGET := iphone:clang:12.2:9.3

include $(THEOS)/makefiles/common.mk

BUNDLE_NAME = KTRPrefs
$(BUNDLE_NAME)_FILES = KTRRootListController.m
$(BUNDLE_NAME)_INSTALL_PATH = /Library/PreferenceBundles
$(BUNDLE_NAME)_FRAMEWORKS = UIKit
$(BUNDLE_NAME)_EXTRA_FRAMEWORKS = Cephei CepheiPrefs
$(BUNDLE_NAME)_PRIVATE_FRAMEWORKS = Preferences
$(BUNDLE_NAME)_LIBRARIES = applist

include $(THEOS_MAKE_PATH)/bundle.mk

internal-stage::
	$(ECHO_NOTHING)mkdir -p $(THEOS_STAGING_DIR)/Library/PreferenceLoader/Preferences$(ECHO_END)
	$(ECHO_NOTHING)cp entry.plist $(THEOS_STAGING_DIR)/Library/PreferenceLoader/Preferences/KTRPrefs.plist$(ECHO_END)
