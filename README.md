# asg-2019
This is a OVE workspace for [All Systems Go 2019](https://cfp.all-systems-go.io).

# The oneliner

    curl -sSL https://raw.githubusercontent.com/Ericsson/ove/master/setup | bash -s asg https://github.com/mtempling/asg-2019

The above oneliner is short for:

    mkdir -p asg
    cd asg
    git clone https://github.com/Ericsson/ove.git .ove
    git clone https://github.com/mtempling/asg-2019
    ln -s asg-2019 .owel
    ln -s .ove/ove ove

# Setup the environment

    source ove

# Open ASG talks in your preferred web browser

    ove asg <tab><tab>

# Fetch some repositories

    ove fetch bat diskus hexyl ripgrep tokei
    ove fetch <tab><tab>

# Fetch all repositories
Here we will issue ~45 git clones (~3GB of disk space) in parallel. You have been warned!

    ove fetch

# Build
Build some Rust programs that was mentioned in the [Alternatives to standard utilities](https://cfp.all-systems-go.io/ASG2019/talk/JFC7VC/) lightning talk.

    ove buildme [<tab><tab>]
    # wait
    tree stage
    stage
    └── usr
        └── bin
            ├── bat
            ├── diskus
            ├── hexyl
            ├── rg
            └── tokei

# Other
The 'schedule' file was fetched (2019-09-23) using:

    curl https://cfp.all-systems-go.io/ASG2019/schedule/export/schedule.json | jq -r .schedule.conference | ...

[OVE](https://github.com/Ericsson/ove)
