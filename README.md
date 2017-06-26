# docker-tensorflow-jupyter

It's a docker for running tensorflow jupyter notebook.

You can find me here. --> https://github.com/volnet/docker-tensorflow-jupyter.git

## Get started

The next scripts can help you to run `jupyter notebook` and `tensorboard` at one time:

```
git clone https://github.com/volnet/tensorflow-server.git
cd tensorflow-server
./tf_start_all.sh
```

You can stop all of them by :

```
./tf_stop_all.sh
```

## How to run

The shell script can help you to run docker:

```
docker run -d -p 8888:8888 -v $(pwd)/notebooks:/notebooks -v $(pwd)/logs:/logs --name my-tf-notebook volnet/tensorflow-jupyter
```

## How to use

You can run jupyter notebook in browser by http://localhost:8888 in the host machine.

## Share folders

I share the `notebooks` and `logs` folders from host to docker by volume parameter.

You can use the `writer = tf.summary.FileWriter('../logs', sess.graph)` to save the graph data to `../logs` folder.

