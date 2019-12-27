##### Sublime Text 3 Install
	
	1- $ wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
	2- $ sudo apt-get install apt-transport-https
	3- $ echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list
	4- $ sudo apt-get update
	5- $ sudo apt-get install sublime-text

##### Uninstall Sublime Text 3

	sudo apt-get remove sublime-text && sudo apt-get autoremove


##### Change font size of the file sidebar

	https://medium.com/vunamhung/sublime-text-3-how-to-change-the-font-face-of-the-file-sidebar-ab358223c695


##### BracketHighter

	{
	"search_threshold":70000,
	 "auto_selection_threshold" : 1000,
	 "content_highlight_bar": true,
	 "align_content_highlight_bar": true,
		"bracket_styles": {
			"curly": {
			    "icon": "curly_bracket",
			     "color": "brackethighlighter.curly",
			     "style": "underline"
			},
		}
	}


##### Common Setting

	{
		"always_prompt_for_file_reload": true,
		"always_show_minimap_viewport": true,
		"bold_folder_labels": true,
		"line_padding_bottom": 3,
		"line_padding_top": 3,
		"highlight_line": true,
		"word_separators": "./\\()\"'-:,.;<>~!@#%^&*|+=[]{}`~?",
		"font_size": 11,

		"font_face": "Menlo",
		
		"color_scheme": "Packages/Colorsublime - Themes/EditPlus.tmTheme",
		"soda_classic_tabs": true,
		"theme": "Soda Light 3.sublime-theme"

		"ignored_packages":
		[
			"Vintage"
		],
		"indent_guide_options":
		[
			"draw_normal",
			"draw_active"
		],

	}


##### Reindent Shortcut

	menu Preferences - Keybindings-User

	[
	    { "keys": ["f12"], "command": "reindent"} 
	]

	select all then F2 reindent entire page


##### toggle_side_bar

	Preferences > Key Bindings - User:
	[
	    { "keys": ["f1"], "command": "toggle_side_bar" }
	]


##### Short Cuts


	Keys		| Description
	----------------|--------------------
	Ctrl+Zero	|	to focus on the side bar
	Ctrl+m   	|	between matching brackets


##### Install Package control

	https://packagecontrol.io/installation







