### TubeTK的血管注释文件说明

TubeTK在109个图像样本中，提供了其中42个样本的辅助数据，即有42个样本有血管注释。这些注释是在一个'.tre'文件中，文件内对血管中心线的每个点记录了坐标和半径。

具体来说，每个注释文件的前12行是总体的参数说明，其中第5行是"ID"，它代表了这个文件有多少组注释。每组的注释都是紧接着的，其中组内注释的形式是，前15行是参数说明，其中组内参数的第14行是"NPoints"，代表这组注释内有多少个点，然后从第16行开始有NPoints行，是每个点的信息。每个点的注释行前四个值分别是$ (x, y, z, r) $，代表三维的坐标和半径。我们需要根据这个来转换成矩阵。
