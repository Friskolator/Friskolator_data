
This is a data-drop for Friskolator Data!

Format is 
	event_name/ Folder is the date of the friskolator event
	event_name/frisks/ UUID.json - Frisk File Each file is a UUID of main frisk event, containing data *only from during that frisk*. Data format specifed below
	event_name/misc/.*UUID.*.json - This is user-generated data from UUID's. Croudsourced ID of object, info, locations of things in photos, etc can be dumped here.  As long as the UUID is somewhere in the name, we will try to associate and parse it. Suggested nameing is UUID.underscore_sep_note.json
	event_name/summary/ *.* This will contain generated png' GIF's and other data. We will update this selectivly, and we will accept NO PULL REQUESTS FOR SUMMARY unless you email us in advance, and explain your magic sauce you want to add, and only if hthe code to make that tasty sauce is in the main Friskolator codebase. 

### Adding Data
 Fork. Pull-request. Repeat.

### Main UUID format.
 For the main UUID's from frisk events, we have a very standard format.  There are some key items we *must* include to make it a valid frisk-event.

Below is an example friskolator-data json file. 

	UUID = { 
	"Version":"0.5" # data version. Used for forward compatiblity
	"img":"flickr_url_of_frisk_image"
	"twitter":"@fakeperson"
	"homeplace":"String, or Lat/Long of home"
	"at":"location of friskolator event"
	"consented":true #MUST_BE_TRUE. ALWAYS.
	"metadata": { 
		# optional metadata block. 
		# not yet defined. Feel free to make
		# messes here
	}

	}
