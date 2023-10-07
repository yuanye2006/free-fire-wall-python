# free-fire-wall-python
中文版：
# 网络监控与阻止器

本仓库包含一个Python脚本，用于监控系统上的网络流量和活动连接数。当网络流量或连接数超过指定阈值时，脚本会自动阻止新的传入连接和特定端口。当流量和连接数回到正常水平时，它将解除对连接和端口的阻止。

## 功能
- 实时监控网络流量（以MB/s为单位）和活动连接数。
- 基于网络流量和连接数阻止和解除对新IP连接的阻止。
- 阻止和解除对指定端口的阻止。
- 恢复启动前的策略配置

## 依赖项
- Python 3.x
- psutil

## 使用

1. **设置阈值和端口**
   - 在脚本中更新 `THRESHOLD_TRAFFIC`、`THRESHOLD_CONNECTIONS` 和 `PORTS_TO_BLOCK` 为您想要的值。

2. **运行脚本**
   
   python 文件名.py
   

3. **监控流量和连接**
   - 脚本将实时输出当前网络流量和连接数到控制台。
   - 当流量或连接超过阈值时，它会阻止新的IP连接和指定的端口，并向控制台输出消息。
   - 当流量和连接恢复正常时，它会解除对连接和端口的阻止，并向控制台输出消息。

## 函数

- `get_current_traffic()`: 返回当前网络流量。
- `get_current_connections()`: 返回当前网络连接数。
- `block_new_ips()`: 阻止所有新的传入IP连接。
- `unblock_new_ips()`: 解除对所有新的传入IP连接的阻止。
- `block_ports(ports)`: 阻止指定的端口列表。
- `unblock_ports(ports)`: 解除对指定端口列表的阻止。

## 示例输出

```plaintext
当前流量输入：0.02 MB/s，当前连接数：80
当前流量输入：0.03 MB/s，当前连接数：82
检测到高流量或连接数！阻止新的IP和指定端口...
当前流量输入：0.01 MB/s，当前连接数：70
流量和连接数恢复正常。解除阻止...
```

## 贡献
随时可以分叉此仓库，进行更改，并提交拉取请求。欢迎任何贡献！

## 许可证
该项目是开源的，并在MIT许可证下提供。

英文版：
# Network Monitor and Blocker

This repository contains a Python script that monitors network traffic and the number of active connections on a system. When either the network traffic or the number of connections exceeds a specified threshold, the script automatically blocks new incoming connections and specific ports. When the traffic and connection count return to normal levels, it unblocks the connections and ports.

## Features
- Real-time monitoring of network traffic (in MB/s) and the number of active connections.
- Blocking and unblocking of new IP connections based on network traffic and connection count.
- Blocking and unblocking of specified ports.

## Dependencies
- Python 3.x
- psutil

## Usage

1. **Setting Thresholds and Ports**
   - Update `THRESHOLD_TRAFFIC`, `THRESHOLD_CONNECTIONS`, and `PORTS_TO_BLOCK` in the script with your desired values.

2. **Running the Script**

   python network_monitor.py
  

3. **Monitoring Traffic and Connections**
   - The script will output the current network traffic and the number of connections to the console in real-time.
   - When traffic or connections exceed the thresholds, it will block new IP connections and the specified ports, and output a message to the console.
   - When traffic and connections return to normal, it will unblock the connections and ports, and output a message to the console.

## Functions

- `get_current_traffic()`: Returns the current network traffic.
- `get_current_connections()`: Returns the current number of network connections.
- `block_new_ips()`: Blocks all new incoming IP connections.
- `unblock_new_ips()`: Unblocks all new incoming IP connections.
- `block_ports(ports)`: Blocks the specified list of ports.
- `unblock_ports(ports)`: Unblocks the specified list of ports.

## Example Output

```plaintext
Current traffic input: 0.02 MB/s, Current connections: 80
Current traffic input: 0.03 MB/s, Current connections: 82
High traffic or connection count detected! Blocking new IPs and specified ports...
Current traffic input: 0.01 MB/s, Current connections: 70
Traffic and connection count are back to normal. Unblocking...
```

## Contributing
Feel free to fork this repository, make changes, and submit pull requests. Any contributions are welcome!

## License
This project is open-source and available under the MIT License.
