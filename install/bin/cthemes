# Init
if [[ $1 = 'set-theme' ]];then
	shell=$2
	theme_name=$3
	theme_dir=$HOME'/.cthemes/themes'
elif [[ $1 = 'info' ]]; then
	echo 'Name: '$themeName
	echo 'Description: '$themeDesc
	echo 'By: '$themeAuthor
	exit
else
	echo 'Operation not supported'
	exit 1
fi

# Mount the theme
source $(echo $theme_dir'/'$theme_name'.ctheme')


# Check if shell is supported
if [[ " ${shells[*]} " =~ " $shell " ]]; then

	# Load Zsh theme
	if [[ $shell = 'zsh' ]];then
		zshTheme
	fi

	# Load Bash theme
	if [[ $shell = 'bash' ]];then
		bashTheme
	fi

	# Load Fish theme
	if [[ $shell = 'fish' ]];then
		fishTheme
	fi
else
	echo 'Theme does not support selected shell'
	exit 1
fi
