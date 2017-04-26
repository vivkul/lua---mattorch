This is mattorch version for lua 5.2

DEPENDENCIES:
Torch7 (www.torch.ch)

INSTALL:
First find "matlab_root" by following command in matlab command line
> matlabroot

Now install using following commands:
$ git clone https://github.com/vivkul/lua---mattorch.git
$ cd lua---mattorch
$ mkdir build
$ cd build
$ cmake -DMATLAB_ROOT=matlab_root ..
$ cd ..
$ luarocks make


USE:
$ th
> require 'mattorch'
-- save:
> tensor1 = torch.Tensor(...)
> tensor2 = torch.Tensor(...)
> tensor3 = torch.Tensor(...)
> mattorch.save('output.mat', tensor1)
-- OR
> list = {myvar = tensor1, othervar = tensor2, thisvar = tensor3}
> mattorch.save('output.mat', list) ]]

-- load:
> loaded = mattorch.load('input.mat')
