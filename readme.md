Notice: remember add this line to /etc/portage/make.conf
PORTDIR_OVERLAY="${PATH_TO_THIS_DIR}"

at target directory
mkdir profiles
mkdir metadata
echo masters = gentoo >> metadata/layout.conf
pwd | sed '/.*\///g' >> profiles/repo_name
echo PORTDIR_OVERLAY=${PWD} >> /etc/portage/make.conf
