See `frameworks/centaur` for **Centaur** framework.


Ubiquitous devices, such as sensing wearables or mobile cameras, provide access to a diverse set of data. However,
the mobility demand for ubiquitous devices naturally imposes constraints on their computational and communication capabilities.
An emerging approach is to locally learn knowledge from data captured by ubiquitous constrained devices (UCDs), rather
than to store and transmit the data in its original form. In this paper, we develop a federated learning framework, called
Centaur, to incorporate on-device data selection on UCDs, which allows partition-based training of a deep neural network through
collaboration between a constrained device and a resourceful device within the multidevice ecosystem of the same user. We
evaluate on five benchmark models and six benchmark datasets that include image and wearable sensor data. On average,
Centaur achieves ∼19% higher accuracy and ∼58% lower latency; compared to the baseline. Moreover, we evaluate Centaur when dealing with imbalanced non-iid data, client participation
heterogeneity, and mobility patterns.

![](./figs/centaur/_overview.png)

![](./figs/centaur/_results_1.png)

![](./figs/centaur/_results_2.png)


#### How to run the code:
(a) **Prerequisites**: Please see `requirements.txt`
> Note that, there might be a problem with older versions of the Flower framework: a problem when running a simulation with ray>=1.12. Ray workers will go into Ray::IDLE mode, which occupies CUDA memory and leads to OOM. For using ray>=1.12 only, a workaround is to change all ray.remote as ray.remote(max_calls=1) in the Flower's ray_client_proxy file.

(b) To Run:
    
        i. Make sure to create directories: `log` nd `results`
        ii. Set up the desired parameters in `unning_args.py`
        ii. Run `python main.py`
(c) For replicating some of the results, run the following command to generate bash scripts: `python make_script.py` and then run specific `.sh` file.


        



