# my_tldr

pip3 install tldr
tldr -u
tldr --print-completion zsh | sudo tee /usr/local/share/zsh/site-functions/_tldr

mkdir ~/.mytldr
touch ~/.mytldr/new_command.md
source_dir="~/.mytldr"; dest_dir="~/.cache/tldr/pages/common"; for file in "$source_dir"/*; do filename=$(basename "$file"); ln -s "$file" "$dest_dir/$filename"; done
tldr new_command
