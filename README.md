# px4_ws
git clone https://github.com/iamrajee/px4_ws.git --recursive

# simple way to add orignal submodule
git submodule add https://github.com/PX4/PX4-Autopilot src/PX4-Autopilot
git submodule add https://github.com/PX4/PX4-SITL_gazebo.git src/PX4-SITL_gazebo/
git add .
git commit -m "added orignal submodule"
git push origin main

## (Advanced??)Add own submodule
cd ~/px4_ws/src/PX4-Autopilot
git config --file=.gitmodules submodule.Submod.url https://github.com/iamrajee/PX4-Autopilot.git
git config --file=.gitmodules submodule.Submod.branch Development
git submodule sync

??
git add .gitmodules
git commit -m "modified submodule URL"
cd ~/px4_ws
git submodule add https://github.com/iamrajee/PX4-Autopilot.git src/PX4-Autopilot
git add .
git commit -m "Added submodule PX4-Autopilot"
git push origin main

# remove pushed folder in own github
git rm --cached src/PX4-Autopilot

# update submodule
?? git submodule update --init --recursive