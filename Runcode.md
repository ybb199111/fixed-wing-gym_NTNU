- 激活虚拟环境

```bash
source Python-3.7.17/path/to/your/venv/bin/activate
```

- 关闭虚拟环境

  ```bash
  deactivate
  ```

进入examples目录

```bash
  cd gym_fixed_wing/examples
```

进入models目录

tensorboard --logdir gym_fixed_wing/examples/models/ppo_example/tb


配置进阶环境

```bash
pip install -r requirements.txt
```

  2.4 运行验证示例程序

```bash
python evaluate_controller.py test_sets/test_set_wind_none_step20-20-3.npy --num-envs 18 --PID --env-config-path fixed_wing_config.json --turbulence-intensity "none"
```

```bash
python evaluate_controller.py test_sets/test_set_wind_none_step20-20-3.npy --num-envs 18 --PID --env-config-path fixed_wing_config.json --turbulence-intensity "none"
```

- 2.5 运行训练示例程序

```
python train_rl_controller.py "ppo_example" 18 --test-set-path test_sets/test_set_wind_none_step20-20-3.npy
```
