# demo_dbcppp

Fork of this [demo](https://github.com/xR3b0rn/dbcppp/blob/master/examples/BasicUsage/main.cpp)
to test [dbcppp](https://github.com/xR3b0rn/dbcppp) within a [colcon workspace](https://colcon.readthedocs.io/en/released/user/quick-start.html).

## Prepare your workspace

In an ubuntu focal box:

- Install `colcon` following the instructions from [here](https://colcon.readthedocs.io/en/released/user/installation.html).
- Create a worksapce:

```sh
mkdir -p my_workspace/src
cd my_workspace/src
```

- Clone `dbcppp` and this repository:

```sh
git clone git@github.com:xR3b0rn/dbcppp.git
git clone git@github.com:agalbachicar/demo_dbcppp.git
```

- Change directory and build with `colcon`:

```sh
cd ..
colcon build --event-handlers console_direct+
```

- Source the install-space:

```sh
source install/setup.bash
```

- Run the example:

```sh
# Run `whereis demo_dbcpp` if you want to see the full path the executable.
demo_dbcpp
```
