# k3s-openfaas

Experiment with k3s on a Raspberry Pi 2 - Model B   
https://blog.alexellis.io/test-drive-k3s-on-raspberry-pi/

```
// SSH into the Rasbperry
$ ssh pi@raspberrypi.local
```

```
// Bootstrap the k3s server
$ curl -sfL https://get.k3s.io | sh -
```

```
// Clone this repository
$ git clone git@github.com:MaartenDesnouck/k3s-openfaas.git
```

```
// Deploy the function
$ ./deploy.sh
```

```
// Check deployment status
$ kubectl get pods
```

```
// Call the function
$ echo -n "Hello world." | curl --data-binary @- http://192.168.1.123:31111
```
