# Git

[Global .gitignore file](http://egorsmirnov.me/2015/05/04/global-gitignore-file.html#:~:text=%20In%20order%20to%20start%20using%20it%2C%20go,page%20at%20git-scm.com%20this%20command%20will...%20More%20)

`touch ~/.gitignore_global`

    # Edit at https://www.toptal.com/developers/gitignore?templates=macos

    ### macOS ###
    # General
    .DS_Store
    .AppleDouble
    .LSOverride

    # Icon must end with two \r
    Icon


    # Thumbnails
    ._*

    # Files that might appear in the root of a volume
    .DocumentRevisions-V100
    .fseventsd
    .Spotlight-V100
    .TemporaryItems
    .Trashes
    .VolumeIcon.icns
    .com.apple.timemachine.donotpresent

    # Directories potentially created on remote AFP share
    .AppleDB
    .AppleDesktop
    Network Trash Folder
    Temporary Items
    .apdisk

    # End of https://www.toptal.com/developers/gitignore/api/macos

`git config --global core.excludesfile ~/.gitignore_global`

## Generate ignore files

[gitignore.io](https://www.toptal.com/developers/gitignore)

