# Changelog

## v2.0.0
### Feature
* Add subtitle keyboard shortcuts (e91322e2d48ed8f1b9ca0916da1612cc0c548b94, bfd54da2c5ea815700da5a0590443b3f27ccefd4)
* Add generic property accessor APIs (ec2fe74a8b6aa6ed2c55d3c27b3314dd70f88fdc)
* Add tooltips for many UI elements (5aad80701459899362b6690ffa84e66cce2bac86)
* Add common keyboard shortcuts for volume & seeking (1e93a73a7f75a194125baee2662e70f1cce617e0)
* Add ? keyboard shortcut for showing known shortcuts (3b24593342184442094fc10f95cc38e11fa754d1)
* Return chapter-list in status (80bb84e2a3598482c0cfbe468ce5d30d231c9c2f)
* Set tooltip text on sliders dynamically (8d6e6bb523302b07949f59fe5d003dde06534f15)
* Update mediaSession playback state & position info (1174ed5272257567707ec000846513af5edc77f6)
* Refresh UI quicker when user is interacting (1369620e3863e53896e8890faa5933c5bbb711c3)
* Allow Esc key to close the playlist (97959f846b9f99e3ccedd2f7016b6c7484e03e8c)
* Lower refresh rate when page is not active (fac4bc64c942567c2e21dfcbf54d7d17fd91d8b7)
* Add option to disable osd logging (2c3c3a5bc36948a2221965ac375027072666faed, ea3540b81d66556b3b3d1b5680574d5631bce113)
* Collapse speed_{faster,slower} into speed_adjust (3be344260506c06d392500ce7dfa2b77bed5dd0f)
* Add a quit API to exit mpv (118db98ca9fadade8d164b55a7140977635e22ab)
* Add playback speed controls (18d52792adcbd8337d8c44194418086734ad2035)
* Include username in log (06857093b3a9964b88f74bc19a5d02c790832041)
* Make htpasswd path configurable (3b3c95d8bfe3df30a6a3b821ba7e0ddefac6b115)

### Fix
* Prevent linebreaks in the repeat button (097aa400ddda7e21075edad719b1ca0c0ccfe857)
* Fix fast touches (4f09d5b820e2c7c7d200fbef32242a011c9adb6c)
* Use `mp.commandv` where possible (1b00430f322ae47ae4ce4d01a6c74b5956327b52)
* Do not capture modified shortcuts (05cf5b63895a08139e4782e6d080fcf6b04fc271)
* Only use setPositionState if available (3db9bed3f6bea381e49be6fa21f3785966774ebf)
* Add missing code blocks to example commands (82000f07b2ce4715ca81e1ae536f3e7189d1f629)
* Update path to favicons (763ccc995d11c96a5e7d58a0e90c13009ce244c3)
* Fix handling missing htpasswd (5692370933d4efe9df1bfb1a39c2cb71132889d8)

### Breaking
* .htpasswd file is not auto-detected anymore. This change is needed, because there are users that have the webui installed through a package manager. This makes adding the file to the directory where `webui.lua` cumbersome.  (3b3c95d8bfe3df30a6a3b821ba7e0ddefac6b115)

### Documentation
* Update screenshots (bee44a035e6acb602fa8fa03230c8a6b0ca7e1b0)
* Improve htpasswd error message & documentation (c5f9c7c9fbf99bb2d3b021a630580bfb04981131)
* Add docs about htpasswd_path (d6a125b360643dd5a8290db8258872e1c35e8cad)

### Thanks
Thanks a lot to @vapier for the contributions to this release!


## v1.1.0
### Feature
* add static_dir configuration (280d5a6e8ef4b562e454c0447ba483ce9bb2acab)

### Fix
* rebuild audio-devices during runtime (637006838aba850bcbfdd837f7e5186b9cec44ba)
* fix display of error message if server fails to start (2c3eb9e2d231ddf872dd297b1f9bc5d33583a985)


## v1.0.0
### Feature
* allow lower case header names (d37a27a8dc67e09a890130d7651602eef871c907)
* include audio-device information in status response (c81cf3b402726a97492639c7651b794f0570c388)

### Fix
* use floats in status json (51ee82143fdc8e61df80dc378f01bbf5c7467d47)
* also print startup_msg to shell (4825a7733f6e52e283f23944f127b6376225028b)
* fix loop handling in frontend (42b3704cb84ac8b0df12e9fae12536ad32539981)
* fix audio-device cycling when audio_devices option is not provided (7e00756ce4c2ca573bc2afc1ba67d45f5ceb3161)

### Breaking
* The type of the duration and volume properties has changed from string to float in the status response.  (51ee82143fdc8e61df80dc378f01bbf5c7467d47)

### Documentation
* fix json in readme (cd8272c093550d524e66604cc6606ee7bc87c831)
* delays are transmitted in seconds, not ms (2b9d23b8091cf6067722970cffcbc2cf7d2a71ae)
* fix typo `audio-devices`/`audio_devices` (c83b9949dabfe1b10c21329cb221f725f9746677)
* fix typo `audio-devices`/`audio_devices` (4fc63269ef84f25a2e7a5d510508f5c91aa7b981)


## v0.3.1
### Fix
* fix reference to audio-devices-list property (604797d24b6009f51a156f889f23df6b71d80d26)

## v0.3.0
### Feature
* add "audio-support" to status response (c66a29f01165446b34a798774165e4d4f12f7374)
* do not round time and volume values (cabf7dbe297a1161aa555bb4de3ded13628225ce)
* hide chapter controls if media has no chapters (8974f9405ca8a92e75da4a23a7b28b8cffe2867f)
* add more key bindings (95243d449eea2e70c5bf84ca329e66d6d2a491b3)

### Documentation
* add a section with a link to windows dependencies repo (10db3814aae26c9a3e496c77a3ad11b5c6f8585e)


## v0.2.1
### Fix
* fix playlist_move validation (7500b4f8819964b9f7e47edd8ae494a697ce4899)
* use events for sending startup notification (067eb23f2c8a3cbe1d395198d60479f95bdf4f12)


## v0.2.0
### Feature
* restyle range input sliders (d2a8a696413faccc275ab4abe2a0dcb5adc6262e)
* add more controls to playlist (2e47afa4fd8c78bcda9a8ac250bded1ee58733d3)
* add playlist_move endpoint (43197eb637a4f4bef9cf1a13d2be528babbe3362)
* refactor playlist controls; add more buttons (7ba4e26d905c9d0ea4cb18ff386c30e930329a4e)
* display chapter info and handle missing chapters (923570ea62a963e3a38204820d856690d7f61aeb)

### Fix
* fix referencing values not present (cf63945e1bf4b01f10a479335e2bde9cda457b0b)
* do not call status() after playlist jump (de21e17e69976fb667bfd816664fb5ae70d7ca17)
* handle empty requests and query params (5c7da039080252144a071aaebbef00cbffcd8409)


## v0.1.0
### Feature
 - Add chapter seeking buttons [#6](https://github.com/open-dynaMIX/simple-mpv-webui/pull/6) *Thanks to @Nebukadneza!*

### Fix
 - prevent zoom-in on double-click [#8](https://github.com/open-dynaMIX/simple-mpv-webui/pull/8)  *Thanks to @rofrol!*
 - Log a warning if a property could not be fetched from mpv [
0d42e81](https://github.com/open-dynaMIX/simple-mpv-webui/commit/0d42e81baa849af969f9dbf803f763106ca9d4e1)


## v0.0.1

Initial release.
