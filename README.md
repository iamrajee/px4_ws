# px4_ws

## Add submodule
cd ~/px4_ws/src/PX4-Autopilot
git config --file=.gitmodules submodule.Submod.url https://github.com/iamrajee/PX4-Autopilot.git
git config --file=.gitmodules submodule.Submod.branch Development
git submodule sync

??
git add .gitmodules
git commit -m "modified submodule URL"
cd ~/px4_ws
git submodule add https://github.com/iamrajee/PX4-Autopilot src/PX4-Autopilot
git add .
git commit -m "Added submodule PX4-Autopilot"
git push origin main


git rm --cached src/PX4-Autopilot