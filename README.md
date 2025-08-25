## 接口目录

- [1.1 根路径检查](#11-根路径检查) - `GET /`
- [1.2 统一任务状态查询](#12-统一任务状态查询) - `GET /api/task/{task_id}`
- [1.3 视频解析](#13-视频解析) - `POST /api/video/parse`
- [2.1 用户注册](#21-用户注册) - `POST /api/user/register`
- [2.2 用户登录](#22-用户登录) - `POST /api/user/login`
- [2.3 刷新访问令牌](#23-刷新访问令牌) - `POST /api/user/refresh`
- [2.4 获取用户资料](#24-获取用户资料) - `GET /api/user/profile`
- [2.5 修改密码](#25-修改密码) - `PUT /api/user/password`
- [2.6 获取功能积分信息](#26-获取功能积分信息) - `GET /api/user/credits/features`
- [2.7 获取积分套餐列表](#27-获取积分套餐列表) - `GET /api/user/credits/packages`
- [2.8 添加作品](#28-添加作品) - `POST /api/user/materials/works/add`
- [2.9 移除作品](#29-移除作品) - `DELETE /api/user/materials/works/remove`
- [2.10 添加数字人素材](#210-添加数字人素材) - `POST /api/user/materials/digital-human/add`
- [2.11 移除数字人素材](#211-移除数字人素材) - `DELETE /api/user/materials/digital-human/remove`
- [2.12 添加背景素材](#212-添加背景素材) - `POST /api/user/materials/background/add`
- [2.13 移除背景素材](#213-移除背景素材) - `DELETE /api/user/materials/background/remove`
- [2.14 添加音色](#214-添加音色) - `POST /api/user/materials/voice/add`
- [2.15 移除音色](#215-移除音色) - `DELETE /api/user/materials/voice/remove`
- [2.16 添加BGM素材](#216-添加bgm素材) - `POST /api/user/materials/bgm/add`
- [2.17 移除BGM素材](#217-移除bgm素材) - `DELETE /api/user/materials/bgm/remove`
- [2.18 获取用户列表](#218-获取用户列表) - `GET /api/user/admin/users`
- [2.19 更新用户信息](#219-更新用户信息) - `PUT /api/user/admin/users/{user_id}`
- [2.20 删除用户](#220-删除用户) - `DELETE /api/user/admin/users/{user_id}`
- [2.21 重置用户密码](#221-重置用户密码) - `PUT /api/user/admin/users/{user_id}/reset-password`
- [2.22 更新用户积分](#222-更新用户积分) - `PUT /api/user/admin/users/{user_id}/credits`
- [2.23 获取用户统计信息](#223-获取用户统计信息) - `GET /api/user/admin/stats`
- [2.24 获取积分消耗图表数据](#224-获取积分消耗图表数据) - `GET /api/user/admin/credits-chart`
- [2.25 获取功能积分配置](#225-获取功能积分配置) - `GET /api/user/admin/credits/features`
- [2.26 编辑功能积分消耗](#226-编辑功能积分消耗) - `PUT /api/user/admin/credits/features/{feature_key}`
- [2.27 获取积分套餐配置](#227-获取积分套餐配置) - `GET /api/user/admin/credits/packages`
- [2.28 新增积分套餐](#228-新增积分套餐) - `POST /api/user/admin/credits/packages`
- [2.29 编辑积分套餐](#229-编辑积分套餐) - `PUT /api/user/admin/credits/packages/{package_key}`
- [2.30 删除积分套餐](#230-删除积分套餐) - `DELETE /api/user/admin/credits/packages/{package_key}`
- [2.31 管理员手动充值积分](#231-管理员手动充值积分) - `POST /api/user/admin/users/{user_id}/credits/recharge`
- [3.1 激活卡密](#31-激活卡密) - `POST /api/cards/activate`
- [3.2 获取我的积分交易记录](#32-获取我的积分交易记录) - `GET /api/cards/my-transactions`
- [3.3 获取我的积分统计](#33-获取我的积分统计) - `GET /api/cards/my-stats`
- [3.4 批量生成卡密](#34-批量生成卡密) - `POST /api/cards/admin/generate`
- [3.5 获取卡密列表](#35-获取卡密列表) - `GET /api/cards/admin/list`
- [3.6 删除卡密](#36-删除卡密) - `DELETE /api/cards/admin/{card_id}`
- [3.7 获取卡密统计](#37-获取卡密统计) - `GET /api/cards/admin/stats`
- [3.8 获取所有积分交易记录](#38-获取所有积分交易记录) - `GET /api/cards/admin/transactions`
- [4.1 搜索用户](#41-搜索用户) - `GET /api/search/users`
- [4.2 搜索积分交易记录](#42-搜索积分交易记录) - `GET /api/search/transactions`
- [4.3 搜索文件](#43-搜索文件) - `GET /api/search/files`
- [4.4 搜索卡密](#44-搜索卡密) - `GET /api/search/cards`
- [5.1 语音合成](#51-语音合成) - `POST /api/tts/synthesize`

- [5.2 获取音色列表](#52-获取音色列表) - `GET /api/tts/voices`
- [5.3 获取音频文件信息](#53-获取音频文件信息) - `GET /api/tts/info/{file_id}`
- [5.4 音色克隆](#54-音色克隆) - `POST /api/tts/voice/clone`
- [5.5 查询音色详情](#55-查询音色详情) - `GET /api/tts/voice/{voice_id}`
- [5.6 更新音色](#56-更新音色) - `PUT /api/tts/voice/{voice_id}`
- [5.7 删除音色](#57-删除音色) - `DELETE /api/tts/voice/{voice_id}`
- [6.1 语音识别处理](#61-语音识别处理) - `POST /api/process`

- [7.1 文本仿写](#71-文本仿写) - `POST /api/llm/rewrite`
- [7.2 获取可用模型列表](#72-获取可用模型列表) - `GET /api/llm/models`
- [8.1 生成视频](#81-生成视频) - `POST /api/videoretalk/generate`

- [8.2 获取视频任务列表](#82-获取视频任务列表) - `GET /api/videoretalk/tasks`
- [8.3 删除视频任务](#83-删除视频任务) - `DELETE /api/videoretalk/task/{task_id}`
- [8.4 绿幕背景替换](#84-绿幕背景替换) - `POST /api/videoretalk/chroma-key`
- [9.1 统一文件上传](#91-统一文件上传) - `POST /api/files/upload`
- [9.2 统一文件下载](#92-统一文件下载) - `GET /api/files/download/{file_id}`
- [9.3 删除文件](#93-删除文件) - `DELETE /api/files/{file_type}/{file_id}`
- [9.4 获取用户文件列表](#94-获取用户文件列表) - `GET /api/files/user/list`
- [9.5 管理员获取所有文件](#95-管理员获取所有文件) - `GET /api/files/admin/list`
- [9.6 获取文件统计信息](#96-获取文件统计信息) - `GET /api/files/stats`
- [9.7 获取缓存文件列表](#97-获取缓存文件列表) - `GET /api/files/cache/list`
- [9.8 获取缓存文件信息](#98-获取缓存文件信息) - `GET /api/files/cache/{file_id}`
- [9.9 删除缓存文件](#99-删除缓存文件) - `DELETE /api/files/cache/{file_id}`
- [10.1 获取最近活动记录](#101-获取最近活动记录) - `GET /api/activities/recent`
- [10.2 获取活动类型](#102-获取活动类型) - `GET /api/activities/types`
- [10.3 获取活动统计信息](#103-获取活动统计信息) - `GET /api/activities/stats`
- [11.1 获取用户任务列表](#111-获取用户任务列表) - `GET /api/tasks/`
- [11.2 获取任务详情](#112-获取任务详情) - `GET /api/tasks/{task_id}`
- [11.3 更新任务](#113-更新任务) - `PUT /api/tasks/{task_id}`
- [11.4 删除任务](#114-删除任务) - `DELETE /api/tasks/{task_id}`
- [11.5 获取任务统计信息](#115-获取任务统计信息) - `GET /api/tasks/stats/summary`
- [11.6 获取所有任务列表](#116-获取所有任务列表) - `GET /api/tasks/admin/all`
- [11.7 获取全局任务统计](#117-获取全局任务统计) - `GET /api/tasks/admin/stats/global`
- [12.1 统一系统状态接口](#121-统一系统状态接口) - `GET /api/system`

---

## 1. 系统基础 API (base.py)

### 1.1 根路径检查
- **路径**: `GET /`
- **描述**: 检查服务是否运行
- **认证**: 无需认证
- **参数**: 无
- **响应示例**:
```json
{
  "message": "服务正在运行"
}
```

### 1.2 统一任务状态查询
- **路径**: `GET /api/task/{task_id}`
- **描述**: 查询各种类型任务的状态（ASR、TTS、视频生成、绿幕处理）
- **认证**: 无需认证
- **参数**:
  - `task_id` (string): 任务ID
- **支持的任务类型**:
  - ASR任务：`task_*` 格式
  - TTS任务：`tts_*` 格式  
  - 视频生成任务：UUID 格式
  - 绿幕处理任务：UUID 格式
- **请求示例**:
```
# TTS任务
GET /api/task/tts_123456789

# 视频生成任务
GET /api/task/uuid-video-task-id

# 绿幕处理任务
GET /api/task/uuid-chroma-key-task-id
```
- **响应示例**（TTS任务）:
```json
{
  "task_id": "tts_123456789",
  "status": "completed",
  "result": {
    "file_id": "audio_12345",
    "file_size_mb": 2.5,
    "format": "wav"
  },
  "created_at": "2024-01-01T10:00:00",
  "completed_at": "2024-01-01T10:01:30"
}
```
- **响应示例**（绿幕处理任务）:
```json
{
  "task_id": "uuid-chroma-key-task-id",
  "status": "SUCCEEDED",
  "message": "绿幕背景替换完成",
  "video_url": "http://...",
  "created_at": "2024-01-01T10:00:00",
  "completed_at": "2024-01-01T10:03:45"
}
```

### 1.3 视频解析
- **路径**: `POST /api/video/parse`
- **描述**: 解析抖音等平台视频链接，获取无水印视频地址
- **认证**: 无需认证
- **请求体**:
```json
{
  "url": "https://v.douyin.com/iXxxxxx/"
}
```
- **响应示例**:
```json
{
  "code": 200,
  "msg": "解析成功",
  "data": {
    "video_url": "https://...",
    "cover_url": "https://...",
    "title": "视频标题",
    "music_url": "https://...",
    "images": [],
    "author": {
      "uid": "123456",
      "name": "作者名",
      "avatar": "https://..."
    }
  },
  "timestamp": "2024-01-01T10:00:00"
}
```

---

## 2. 用户管理 API (user.py)

### 2.1 用户注册
- **路径**: `POST /api/user/register`
- **描述**: 新用户注册
- **认证**: 无需认证
- **请求体**:
```json
{
  "account": "testuser",
  "password": "password123",
  "confirm_password": "password123"
}
```
- **响应示例**:
```json
{
  "id": 1,
  "account": "testuser",
  "is_admin": false,
  "is_active": true,
  "credits": 0,
  "works": [],
  "digital_human_materials": [],
  "background_materials": [],
  "voice_tones": [],
  "bgm_materials": [],
  "created_at": "2024-01-01T10:00:00",
  "updated_at": "2024-01-01T10:00:00",
  "last_login_at": null
}
```

### 2.2 用户登录
- **路径**: `POST /api/user/login`
- **描述**: 用户登录获取访问令牌
- **认证**: 无需认证
- **请求体**:
```json
{
  "account": "testuser",
  "password": "password123"
}
```
- **响应示例**:
```json
{
  "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9...",
  "refresh_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9...",
  "token_type": "bearer",
  "expires_in": 3600
}
```

### 2.3 刷新访问令牌
- **路径**: `POST /api/user/refresh`
- **描述**: 使用刷新令牌获取新的访问令牌
- **认证**: 无需认证
- **请求体**:
```json
{
  "refresh_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9..."
}
```
- **响应示例**:
```json
{
  "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9...",
  "token_type": "bearer"
}
```

### 2.4 获取用户资料
- **路径**: `GET /api/user/profile`
- **描述**: 获取当前用户的详细资料
- **认证**: 需要认证
- **响应示例**:
```json
{
  "id": 1,
  "account": "testuser",
  "is_admin": false,
  "is_active": true,
  "credits": 100,
  "works": ["file_123", "file_456"],
  "digital_human_materials": ["dh_789"],
  "background_materials": ["bg_101"],
  "voice_tones": ["voice_202"],
  "bgm_materials": ["bgm_303"],
  "created_at": "2024-01-01T10:00:00",
  "updated_at": "2024-01-01T10:00:00",
  "last_login_at": "2024-01-01T15:30:00"
}
```

### 2.5 修改密码
- **路径**: `PUT /api/user/password`
- **描述**: 修改当前用户密码
- **认证**: 需要认证
- **请求体**:
```json
{
  "current_password": "oldpassword",
  "new_password": "newpassword123"
}
```
- **响应示例**:
```json
{
  "message": "密码修改成功"
}
```

### 2.6 获取功能积分信息
- **路径**: `GET /api/user/credits/features`
- **描述**: 获取所有需要积分的功能及其消耗情况
- **认证**: 需要认证
- **响应示例**:
```json
{
  "user_credits": 120,
  "features": {
    "tts": {
      "name": "语音合成",
      "credits_cost": 10,
      "available_times": 12,
      "sufficient_credits": true,
      "implemented": true
    },
    "voice_clone": {
      "name": "音色克隆",
      "credits_cost": 50,
      "available_times": 2,
      "sufficient_credits": true,
      "implemented": true
    },
    "video_generate": {
      "name": "视频生成",
      "credits_cost": 100,
      "available_times": 1,
      "sufficient_credits": true,
      "implemented": false
    },
    "chroma_key": {
      "name": "绿幕背景替换",
      "credits_cost": 80,
      "available_times": 1,
      "sufficient_credits": true,
      "implemented": false
    },
    "asr_recognize": {
      "name": "语音识别",
      "credits_cost": 20,
      "available_times": 6,
      "sufficient_credits": true,
      "implemented": false
    },
    "llm_rewrite": {
      "name": "文本仿写",
      "credits_cost": 15,
      "available_times": 8,
      "sufficient_credits": true,
      "implemented": false
    }
  },
  "summary": {
    "total_features": 6,
    "implemented_features": 2,
    "affordable_features": 6,
    "min_cost": 10,
    "max_cost": 100
  },
  "recommendations": [
    {
      "type": "sufficient_credits",
      "message": "您的积分充足，可以使用所有功能",
      "action": "开始使用服务"
    }
  ]
}
```

### 2.7 获取积分套餐列表
- **路径**: `GET /api/user/credits/packages`
- **描述**: 获取所有积分套餐信息（1人民币=100积分）
- **认证**: 需要认证
- **响应示例**:
```json
{
  "user_info": {
    "current_credits": 150,
    "account": "user123"
  },
  "packages": {
    "recharge_1": {
      "name": "1元充值",
      "credits": 100,
      "price_cny": 1.0,
      "discount": 0,
      "popular": false,
      "value_ratio": 100.0,
      "original_price_cny": 1.0,
      "savings_cny": 0.0
    },
    "recharge_6": {
      "name": "6元充值",
      "credits": 600,
      "price_cny": 6.0,
      "discount": 0,
      "popular": false,
      "value_ratio": 100.0,
      "original_price_cny": 6.0,
      "savings_cny": 0.0
    },
    "recharge_30": {
      "name": "30元充值",
      "credits": 3100,
      "price_cny": 30.0,
      "discount": 3.33,
      "popular": true,
      "value_ratio": 103.33,
      "original_price_cny": 31.0,
      "savings_cny": 1.0
    },
    "recharge_68": {
      "name": "68元充值",
      "credits": 7200,
      "price_cny": 68.0,
      "discount": 5.88,
      "popular": false,
      "value_ratio": 105.88,
      "original_price_cny": 72.0,
      "savings_cny": 4.0
    },
    "recharge_128": {
      "name": "128元充值",
      "credits": 14000,
      "price_cny": 128.0,
      "discount": 9.38,
      "popular": false,
      "value_ratio": 109.38,
      "original_price_cny": 140.0,
      "savings_cny": 12.0
    },
    "recharge_328": {
      "name": "328元充值",
      "credits": 36800,
      "price_cny": 328.0,
      "discount": 12.20,
      "popular": false,
      "value_ratio": 112.20,
      "original_price_cny": 368.0,
      "savings_cny": 40.0
    }
  },
  "exchange_rate": {
    "cny_to_credits": 100,
    "description": "1人民币 = 100积分"
  },
  "summary": {
    "total_packages": 6,
    "price_range": {
      "min_price": 1.0,
      "max_price": 328.0
    },
    "credits_range": {
      "min_credits": 100,
      "max_credits": 36800
    }
  }
}
```

### 2.8 素材管理
#### 添加作品
- **路径**: `POST /api/user/materials/works/add`
- **描述**: 添加作品到用户资料
- **认证**: 需要认证
- **注意**: 会验证文件是否存在，不存在的文件将无法添加
- **请求体**:
```json
{
  "file_id": "video_123456"
}
```
- **成功响应**:
```json
{
  "message": "作品添加成功"
}
```
- **错误响应** (文件不存在):
```json
{
  "detail": "文件不存在: video_123456"
}
```

#### 移除作品
- **路径**: `DELETE /api/user/materials/works/remove`
- **描述**: 从用户资料移除作品
- **认证**: 需要认证
- **请求体**:
```json
{
  "file_id": "video_123456"
}
```

#### 添加数字人素材
- **路径**: `POST /api/user/materials/digital-human/add`
- **描述**: 添加数字人素材到用户资料
- **认证**: 需要认证
- **注意**: 会验证文件是否存在，不存在的文件将无法添加
- **请求体**:
```json
{
  "file_id": "dh_123456"
}
```

#### 添加背景素材
- **路径**: `POST /api/user/materials/background/add`
- **描述**: 添加背景素材到用户资料
- **认证**: 需要认证
- **注意**: 会验证文件是否存在，不存在的文件将无法添加
- **请求体**:
```json
{
  "file_id": "bg_123456"
}
```

#### 添加音色
- **路径**: `POST /api/user/materials/voice/add`
- **描述**: 添加音色到用户资料
- **认证**: 需要认证
- **注意**: 音色ID不同于文件ID，此接口不验证文件存在性
- **请求体**:
```json
{
  "file_id": "voice_123456"
}
```

#### 添加BGM素材
- **路径**: `POST /api/user/materials/bgm/add`
- **描述**: 添加BGM素材到用户资料
- **认证**: 需要认证
- **注意**: 会验证文件是否存在，不存在的文件将无法添加
- **请求体**:
```json
{
  "file_id": "bgm_123456"
}
```

### 2.9 管理员功能

#### 获取用户列表
- **路径**: `GET /api/user/admin/users`
- **描述**: 管理员获取所有用户列表
- **认证**: 需要管理员认证
- **参数**:
  - `skip` (int): 跳过数量，默认0
  - `limit` (int): 限制数量，默认100
- **请求示例**:
```
GET /api/user/admin/users?skip=0&limit=10
```

#### 更新用户信息
- **路径**: `PUT /api/user/admin/users/{user_id}`
- **描述**: 管理员更新用户信息
- **认证**: 需要管理员认证
- **请求体**:
```json
{
  "is_active": true,
  "is_admin": false
}
```

#### 删除用户
- **路径**: `DELETE /api/user/admin/users/{user_id}`
- **描述**: 管理员删除用户
- **认证**: 需要管理员认证

#### 重置用户密码
- **路径**: `PUT /api/user/admin/users/{user_id}/reset-password`
- **描述**: 管理员重置用户密码
- **认证**: 需要管理员认证
- **请求体**:
```json
{
  "new_password": "newpassword123"
}
```

#### 更新用户积分
- **路径**: `PUT /api/user/admin/users/{user_id}/credits`
- **描述**: 管理员更新用户积分
- **认证**: 需要管理员认证
- **请求体**:
```json
{
  "credits": 100,
  "operation": "add",
  "reason": "系统赠送"
}
```

#### 获取用户统计信息
- **路径**: `GET /api/user/admin/stats`
- **描述**: 管理员获取用户统计信息
- **认证**: 需要管理员认证

#### 获取积分消耗图表数据
- **路径**: `GET /api/user/admin/credits-chart`
- **描述**: 获取积分消耗图表数据
- **认证**: 需要管理员认证
- **参数**:
  - `hours` (int): 查询最近几小时的数据，默认24，范围1-72

#### 获取功能积分配置
- **路径**: `GET /api/user/admin/credits/features`
- **描述**: 管理员获取所有功能的积分配置
- **认证**: 需要管理员认证
- **响应示例**:
```json
{
  "features": {
    "tts": {
      "name": "语音合成",
      "description": "将文本转换为语音",
      "credits_cost": 10,
      "endpoint": "POST /api/tts/synthesize",
      "unit": "每次合成",
      "category": "语音服务"
    },
    "voice_clone": {
      "name": "音色克隆",
      "description": "基于音频样本创建自定义音色",
      "credits_cost": 50,
      "endpoint": "POST /api/tts/voice/clone",
      "unit": "每次克隆",
      "category": "语音服务"
    }
  },
  "config_info": {
    "total_features": 2,
    "last_updated": "2024-01-01T10:00:00",
    "managed_by": "系统管理员"
  }
}
```

#### 编辑功能积分消耗
- **路径**: `PUT /api/user/admin/credits/features/{feature_key}`
- **描述**: 管理员编辑指定功能的积分消耗
- **认证**: 需要管理员认证
- **参数**:
  - `feature_key` (path): 功能键名 (`tts`, `voice_clone`)
  - `credits_cost` (query): 新的积分消耗（必须≥0）
- **请求示例**:
```bash
PUT /api/user/admin/credits/features/tts?credits_cost=15
```
- **响应示例**:
```json
{
  "message": "功能积分消耗更新成功",
  "feature_key": "tts",
  "feature_name": "语音合成",
  "old_credits_cost": 10,
  "new_credits_cost": 15,
  "updated_by": "admin",
  "updated_at": "2024-01-01T10:00:00"
}
```

#### 获取积分套餐配置
- **路径**: `GET /api/user/admin/credits/packages`
- **描述**: 管理员获取积分套餐配置
- **认证**: 需要管理员认证
- **响应示例**:
```json
{
  "packages": {
    "basic": {
      "name": "基础套餐",
      "description": "适合轻度使用者",
      "credits": 1000,
      "price_cny": 10.0,
      "discount": 0,
      "popular": false,
      "features": ["TTS语音合成", "基础功能使用"],
      "validity_days": 365
    }
  },
  "exchange_rate": {
    "cny_to_credits": 100,
    "description": "1人民币 = 100积分"
  },
  "config_info": {
    "total_packages": 4,
    "last_updated": "2024-01-01T10:00:00",
    "managed_by": "系统管理员"
  }
}
```

#### 新增积分套餐
- **路径**: `POST /api/user/admin/credits/packages`
- **描述**: 管理员新增积分套餐
- **认证**: 需要管理员认证
- **参数**:
  - `package_key` (query): 套餐键名（唯一标识）
  - `name` (query): 套餐名称
  - `credits` (query): 积分数量（≥1）
  - `price_cny` (query): 价格（人民币，≥0.01）
  - `discount` (query): 折扣百分比（0-100，默认0）
  - `popular` (query): 是否为热门套餐（默认false）
  - `sort_order` (query): 排序序号（≥0，默认0）
- **请求示例**:
```bash
POST /api/user/admin/credits/packages?package_key=vip&name=VIP套餐&credits=5000&price_cny=40.0&discount=20&popular=true&sort_order=10
```

#### 编辑积分套餐
- **路径**: `PUT /api/user/admin/credits/packages/{package_key}`
- **描述**: 管理员编辑积分套餐
- **认证**: 需要管理员认证
- **参数**: 同新增积分套餐
- **请求示例**:
```bash
PUT /api/user/admin/credits/packages/basic?name=基础套餐Plus&credits=1200&price_cny=12.0&sort_order=1
```

#### 删除积分套餐
- **路径**: `DELETE /api/user/admin/credits/packages/{package_key}`
- **描述**: 管理员删除积分套餐
- **认证**: 需要管理员认证
- **参数**:
  - `package_key` (path): 套餐键名
- **响应示例**:
```json
{
  "message": "积分套餐删除成功",
  "package_key": "basic",
  "package_name": "基础套餐",
  "deleted_by": "admin",
  "deleted_at": "2024-01-01T10:00:00"
}
```

#### 管理员手动充值积分
- **路径**: `POST /api/user/admin/users/{user_id}/credits/recharge`
- **描述**: 管理员手动给用户充值积分（增加模式）
- **认证**: 需要管理员认证
- **参数**:
  - `user_id` (path): 用户ID
  - `amount` (query): 充值积分数量（≥1）
  - `description` (query): 充值描述（可选，默认"管理员手动充值"）
- **请求示例**:
```bash
POST /api/user/admin/users/5/credits/recharge?amount=1000&description=客服补偿积分
```
- **响应示例**:
```json
{
  "message": "积分充值成功",
  "user_id": 5,
  "user_account": "user123",
  "recharge_amount": 1000,
  "balance_before": 150,
  "balance_after": 1150,
  "description": "客服补偿积分",
  "recharged_by": "admin",
  "recharged_at": "2024-01-01T10:00:00"
}
```

---

## 3. 卡密系统 API (cards.py)

### 用户功能

### 3.1 激活卡密
- **路径**: `POST /api/cards/activate`
- **描述**: 用户使用卡密激活获取积分
- **认证**: 需要认证
- **请求体**:
```json
{
  "card_code": "A2B3C4D5E6F7G8H9"
}
```
- **响应示例**:
```json
{
  "success": true,
  "message": "卡密激活成功",
  "credits_added": 1000,
  "new_balance": 2500,
  "package_name": "基础套餐"
}
```

### 3.2 获取我的积分交易记录
- **路径**: `GET /api/cards/my-transactions`
- **描述**: 获取当前用户的积分交易记录
- **认证**: 需要认证
- **查询参数**:
  - `page` (optional): 页码，默认1
  - `page_size` (optional): 每页数量，默认20
  - `transaction_type` (optional): 交易类型筛选 (card_activation, admin_recharge, feature_consume, admin_deduct)
- **响应示例**:
```json
{
  "transactions": [
    {
      "id": 1,
      "transaction_type": "card_activation",
      "amount": 1000,
      "balance_before": 1500,
      "balance_after": 2500,
      "card_code": "A2B3C4D5E6F7G8H9",
      "feature_key": null,
      "feature_name": null,
      "description": "激活卡密 A2B3C4D5E6F7G8H9，获得 1000 积分（基础套餐）",
      "operator_admin_username": null,
      "created_at": "2024-01-01T10:00:00"
    },
    {
      "id": 2,
      "transaction_type": "feature_consume",
      "amount": -10,
      "balance_before": 2500,
      "balance_after": 2490,
      "card_code": null,
      "feature_key": "tts",
      "feature_name": "语音合成",
      "description": "TTS语音合成消耗积分",
      "operator_admin_username": null,
      "created_at": "2024-01-01T11:00:00"
    }
  ],
  "total": 25,
  "page": 1,
  "page_size": 20,
  "total_pages": 2
}
```

### 3.3 获取我的积分统计
- **路径**: `GET /api/cards/my-stats`
- **描述**: 获取当前用户的积分统计信息
- **认证**: 需要认证
- **响应示例**:
```json
{
  "total_earned": 5000,
  "total_consumed": 250,
  "current_balance": 4750,
  "card_activations": 3,
  "admin_recharges": 1,
  "feature_consumptions": 25,
  "recent_transactions": [
    {
      "id": 1,
      "transaction_type": "card_activation",
      "amount": 1000,
      "balance_before": 1500,
      "balance_after": 2500,
      "card_code": "A2B3C4D5E6F7G8H9",
      "feature_key": null,
      "feature_name": null,
      "description": "激活卡密获得积分",
      "operator_admin_username": null,
      "created_at": "2024-01-01T10:00:00"
    }
  ]
}
```

### 管理员功能

### 3.4 批量生成卡密
- **路径**: `POST /api/cards/admin/generate`
- **描述**: 管理员批量生成卡密
- **认证**: 需要管理员认证
- **请求体**:
```json
{
  "package_key": "basic",
  "quantity": 10,
  "batch_number": "BATCH_20240101_001",
  "description": "新年活动卡密",
  "expires_days": 365
}
```
- **响应示例**:
```json
{
  "success": true,
  "message": "成功生成 10 张卡密",
  "batch_number": "BATCH_20240101120000_1234",
  "generated_count": 10,
  "failed_count": 0,
  "cards": [
    "A2B3C4D5E6F7G8H9",
    "B3C4D5E6F7G8H9J2",
    "C4D5E6F7G8H9J2K3"
  ],
  "total_credits": 10000,
  "total_value": 100.0
}
```

### 3.5 获取卡密列表
- **路径**: `GET /api/cards/admin/list`
- **描述**: 管理员获取卡密列表
- **认证**: 需要管理员认证
- **查询参数**:
  - `page` (optional): 页码，默认1
  - `page_size` (optional): 每页数量，默认20
  - `status` (optional): 状态筛选 (active, used, expired, disabled)
  - `batch_number` (optional): 批次号筛选
  - `package_key` (optional): 套餐筛选
- **响应示例**:
```json
{
  "cards": [
    {
      "id": 1,
      "card_code": "A2B3C4D5E6F7G8H9",
      "package_key": "basic",
      "package_name": "基础套餐",
      "credits": 1000,
      "price_cny": 10.0,
      "status": "used",
      "used_by_user_id": 5,
      "used_by_username": "user123",
      "used_at": "2024-01-01T10:00:00",
      "created_by_admin_id": 1,
      "created_by_admin_username": "admin",
      "batch_number": "BATCH_20240101_001",
      "description": "新年活动卡密",
      "expires_at": "2025-01-01T00:00:00",
      "created_at": "2024-01-01T09:00:00"
    }
  ],
  "total": 50,
  "page": 1,
  "page_size": 20,
  "total_pages": 3
}
```

### 3.6 删除卡密
- **路径**: `DELETE /api/cards/admin/{card_id}`
- **描述**: 管理员删除卡密（只能删除未使用的卡密）
- **认证**: 需要管理员认证
- **参数**:
  - `card_id` (path): 卡密ID
- **响应示例**:
```json
{
  "message": "卡密删除成功"
}
```

### 3.7 获取卡密统计
- **路径**: `GET /api/cards/admin/stats`
- **描述**: 管理员获取卡密统计信息
- **认证**: 需要管理员认证
- **响应示例**:
```json
{
  "total_cards": 100,
  "active_cards": 75,
  "used_cards": 20,
  "expired_cards": 3,
  "disabled_cards": 2,
  "total_credits_value": 75000,
  "total_money_value": 750.0
}
```

### 3.8 获取所有积分交易记录
- **路径**: `GET /api/cards/admin/transactions`
- **描述**: 管理员获取所有用户的积分交易记录
- **认证**: 需要管理员认证
- **查询参数**:
  - `page` (optional): 页码，默认1
  - `page_size` (optional): 每页数量，默认20
  - `transaction_type` (optional): 交易类型筛选
  - `user_id` (optional): 用户ID筛选
- **响应示例**:
```json
{
  "transactions": [
    {
      "id": 1,
      "transaction_type": "card_activation",
      "amount": 1000,
      "balance_before": 1500,
      "balance_after": 2500,
      "card_code": "A2B3C4D5E6F7G8H9",
      "feature_key": null,
      "feature_name": null,
      "description": "激活卡密获得积分",
      "operator_admin_username": null,
      "created_at": "2024-01-01T10:00:00"
    }
  ],
  "total": 1000,
  "page": 1,
  "page_size": 20,
  "total_pages": 50
}
```

---

## 4. 高级搜索 API (search.py)

### 4.1 搜索用户
- **路径**: `GET /api/search/users`
- **描述**: 管理员搜索用户，支持按用户名、账号模糊搜索，支持多种筛选条件
- **认证**: 需要管理员认证
- **查询参数**:
  - `q` (required): 搜索关键词（用户名/账号）
  - `page` (optional): 页码，默认1
  - `page_size` (optional): 每页数量，默认20
  - `is_admin` (optional): 是否管理员筛选
  - `is_active` (optional): 是否激活筛选
  - `credits_min` (optional): 最小积分
  - `credits_max` (optional): 最大积分
- **请求示例**:
```bash
GET /api/search/users?q=user&is_active=true&credits_min=100
```
- **响应示例**:
```json
{
  "users": [
    {
      "id": 5,
      "account": "user123",
      "is_admin": false,
      "is_active": true,
      "credits": 1500,
      "created_at": "2024-01-01T10:00:00",
      "last_login_at": "2024-01-15T08:30:00",
      "works_count": 3,
      "materials_count": 5,
      "voices_count": 2
    }
  ],
  "total": 1,
  "page": 1,
  "page_size": 20,
  "total_pages": 1,
  "search_keyword": "user",
  "filters_applied": {
    "is_active": true,
    "credits_min": 100
  }
}
```

### 4.2 搜索积分交易记录
- **路径**: `GET /api/search/transactions`
- **描述**: 管理员搜索积分交易记录，支持多条件组合搜索
- **认证**: 需要管理员认证
- **查询参数**:
  - `q` (optional): 搜索关键词（用户账号、卡密代码、描述）
  - `page` (optional): 页码，默认1
  - `page_size` (optional): 每页数量，默认20
  - `transaction_type` (optional): 交易类型筛选
  - `user_id` (optional): 用户ID筛选
  - `amount_min` (optional): 最小金额
  - `amount_max` (optional): 最大金额
  - `date_from` (optional): 开始日期 (YYYY-MM-DD)
  - `date_to` (optional): 结束日期 (YYYY-MM-DD)
- **请求示例**:
```bash
GET /api/search/transactions?q=充值&transaction_type=admin_recharge&date_from=2024-01-01
```

### 4.3 搜索文件
- **路径**: `GET /api/search/files`
- **描述**: 管理员搜索文件，支持按文件名模糊搜索，支持多种筛选条件
- **认证**: 需要管理员认证
- **查询参数**:
  - `q` (required): 搜索关键词（文件名）
  - `page` (optional): 页码，默认1
  - `page_size` (optional): 每页数量，默认20
  - `file_type` (optional): 文件类型筛选
  - `user_id` (optional): 上传用户ID筛选
  - `size_min` (optional): 最小文件大小（字节）
  - `size_max` (optional): 最大文件大小（字节）
- **请求示例**:
```bash
GET /api/search/files?q=audio&file_type=backgrounds&size_min=1000000
```
- **响应示例**:
```json
{
  "files": [
    {
      "file_id": "file_123456",
      "original_name": "background_audio.mp3",
      "file_type": "backgrounds",
      "size": 2048000,
      "size_human": "2.0 MB",
      "extension": ".mp3",
      "user_id": 5,
      "user_account": "user123",
      "created_at": "2024-01-01T10:00:00",
      "file_path": "/path/to/file"
    }
  ],
  "total": 1,
  "page": 1,
  "page_size": 20,
  "total_pages": 1,
  "search_keyword": "audio",
  "filters_applied": {
    "file_type": "backgrounds",
    "size_min": 1000000
  }
}
```

### 4.4 搜索卡密
- **路径**: `GET /api/search/cards`
- **描述**: 管理员搜索卡密，支持多条件组合搜索
- **认证**: 需要管理员认证
- **查询参数**:
  - `q` (optional): 搜索关键词（卡密代码、批次号）
  - `page` (optional): 页码，默认1
  - `page_size` (optional): 每页数量，默认20
  - `status` (optional): 卡密状态筛选 (active, used, expired, disabled)
  - `package_key` (optional): 套餐类型筛选
  - `created_admin_id` (optional): 创建管理员ID筛选
  - `used_user_id` (optional): 使用用户ID筛选
  - `date_from` (optional): 创建开始日期 (YYYY-MM-DD)
  - `date_to` (optional): 创建结束日期 (YYYY-MM-DD)
- **请求示例**:
```bash
GET /api/search/cards?q=BATCH_&status=active&package_key=basic
```
- **响应示例**:
```json
{
  "cards": [
    {
      "id": 1,
      "card_code": "A2B3C4D5E6F7G8H9",
      "package_key": "basic",
      "package_name": "基础套餐",
      "credits": 1000,
      "price_cny": 10.0,
      "status": "active",
      "batch_number": "BATCH_20240101_001",
      "description": "新年活动卡密",
      "created_by_admin": "admin",
      "used_by_user": null,
      "used_at": null,
      "expires_at": "2025-01-01T00:00:00",
      "created_at": "2024-01-01T09:00:00"
    }
  ],
  "total": 1,
  "page": 1,
  "page_size": 20,
  "total_pages": 1,
  "search_keyword": "BATCH_",
  "filters_applied": {
    "status": "active",
    "package_key": "basic"
  }
}
```

---

## 5. 语音合成 API (tts.py)

### 3.1 语音合成
- **路径**: `POST /api/tts/synthesize`
- **描述**: 文本转语音合成（异步），消耗10积分
- **认证**: 需要认证
- **请求体**:
```json
{
  "text": "要合成的文本内容",
  "voice": "voice_123456",
  "format": "wav",
  "volume": 80,
  "speech_rate": 1.0,
  "pitch_rate": 1.0
}
```
- **响应示例**:
```json
{
  "task_id": "tts_123456789",
  "status": "processing",
  "message": "语音合成任务已创建，正在处理中"
}
```



### 5.2 获取音色列表
- **路径**: `GET /api/tts/voices`
- **描述**: 获取可用音色列表（包括预设音色和克隆音色）
- **认证**: 无需认证
- **参数**:
  - `type` (string): 音色类型（preset/cloned/all），默认all
  - `prefix` (string): 克隆音色前缀过滤
- **请求示例**:
```
GET /api/tts/voices?type=all&prefix=user_
```
- **响应示例**:
```json
{
  "preset_voices": {
    "female": ["zhichu", "zhixia"],
    "male": ["zhiwei", "zhijie"]
  },
  "cloned_voices": [
    {
      "voice_id": "voice_123456",
      "gmt_create": "2024-01-01T10:00:00",
      "gmt_modified": "2024-01-01T10:00:00",
      "status": "success",
      "owner_user": 1,
      "owner_account": "testuser"
    }
  ],
  "total_count": 6
}
```

### 5.3 获取音频文件信息
- **路径**: `GET /api/tts/info/{file_id}`
- **描述**: 获取音频文件信息
- **认证**: 需要认证
- **参数**:
  - `file_id` (string): 文件ID
- **响应示例**:
```json
{
  "file_id": "audio_12345",
  "file_size": 2621440,
  "file_size_mb": 2.5,
  "format": "wav",
  "exists": true,
  "created_at": "2024-01-01T10:01:30"
}
```

### 5.4 音色克隆
- **路径**: `POST /api/tts/voice/clone`
- **描述**: 创建音色（音色克隆），消耗50积分
- **认证**: 需要认证
- **请求体**:
```json
{
  "audio_url": "http://localhost:8000/api/files/audio/123456/download",
  "prefix": "user_custom",
  "target_model": "sovits"
}
```
- **响应示例**:
```json
{
  "voice_id": "voice_987654321",
  "message": "音色克隆成功"
}
```

### 5.5 查询音色详情
- **路径**: `GET /api/tts/voice/{voice_id}`
- **描述**: 查询指定音色详细信息
- **认证**: 无需认证
- **参数**:
  - `voice_id` (string): 音色ID
- **响应示例**:
```json
{
  "voice_id": "voice_987654321",
  "gmt_create": "2024-01-01T10:00:00",
  "gmt_modified": "2024-01-01T10:00:00",
  "status": "success",
  "resource_link": "http://...",
  "target_model": "sovits"
}
```

### 5.6 更新音色
- **路径**: `PUT /api/tts/voice/{voice_id}`
- **描述**: 更新音色（管理员权限）
- **认证**: 需要管理员认证
- **请求体**:
```json
{
  "audio_url": "http://localhost:8000/api/files/audio/654321/download"
}
```

### 5.7 删除音色
- **路径**: `DELETE /api/tts/voice/{voice_id}`
- **描述**: 删除音色（管理员权限）
- **认证**: 需要管理员认证
- **响应示例**:
```json
{
  "voice_id": "voice_987654321",
  "message": "音色删除成功",
  "deleted_at": "2024-01-01T10:00:00"
}
```

**💡 音色试听**：
音色试听功能已整合到统一文件下载接口，使用以下方式获取：
```bash
# 获取音色试听（无需认证）
GET /api/files/download/voice_preview_{voice_id}.wav
```

---

## 4. 语音识别 API (asr.py)

### 4.1 语音识别处理
- **路径**: `POST /api/process`
- **描述**: 使用Gummy实时语音识别模型处理音频/视频文件进行语音识别
- **认证**: 需要认证
- **模型**: 使用DashScope的gummy-realtime-v1模型，支持中英日韩等多语言识别
- **请求方式**: multipart/form-data
- **参数**:
  - `file` (file): 上传的音频/视频文件（可选）
  - `file_id` (string): 已上传文件的ID（可选）
- **支持格式**: 
  - 音频：WAV, MP3, AAC, M4A, FLAC, PCM, OPUS, SPEEX, AMR
  - 视频：MP4, AVI, MOV, MKV, WMV, FLV
- **技术特性**:
  - 支持实时语音识别和同步文件识别
  - 自动进行标点符号预测和逆文本正则化
  - 使用VAD（Voice Activity Detection）进行智能断句
  - 支持16kHz及以上采样率
- **请求示例**:
```bash
curl -X POST "http://localhost:8000/api/process" \
  -H "Authorization: Bearer <token>" \
  -F "file=@audio.wav"
```
或者
```bash
curl -X POST "http://localhost:8000/api/process" \
  -H "Authorization: Bearer <token>" \
  -F "file_id=audio_123456"
```
- **响应示例**:
```json
{
  "task_id": "abc-123-def-456",
  "status": "completed",
  "message": "处理完成"
}
```



---

## 5. 大语言模型 API (llm.py)

### 5.1 文本仿写
- **路径**: `POST /api/llm/rewrite`
- **描述**: 文本仿写，支持自动和自定义模式
- **认证**: 需要认证
- **请求体**:
```json
{
  "text": "要仿写的原文本",
  "mode": "auto",
  "custom_instruction": "请将文本改写得更正式",
  "length_ratio": 1.2,
  "stream": false
}
```
- **响应示例**（非流式）:
```json
{
  "original_text": "要仿写的原文本",
  "rewritten_text": "仿写后的文本内容",
  "mode": "auto",
  "model": "qwen-plus",
  "usage": {
    "prompt_tokens": 50,
    "completion_tokens": 60,
    "total_tokens": 110
  },
  "stream": false
}
```

### 5.2 获取可用模型列表
- **路径**: `GET /api/llm/models`
- **描述**: 获取可用的LLM模型列表
- **认证**: 无需认证
- **响应示例**:
```json
{
  "models": [
    {
      "id": "qwen-plus",
      "name": "通义千问Plus",
      "description": "阿里云通义千问Plus模型，适合复杂任务"
    },
    {
      "id": "qwen-turbo",
      "name": "通义千问Turbo",
      "description": "阿里云通义千问Turbo模型，响应速度快"
    },
    {
      "id": "qwen-max",
      "name": "通义千问Max",
      "description": "阿里云通义千问Max模型，性能最强"
    }
  ]
}
```

---

## 6. 视频生成 API (videoretalk.py)

### 6.1 生成视频
- **路径**: `POST /api/videoretalk/generate`
- **描述**: 使用VideoRetalk生成数字人视频
- **认证**: 需要认证
- **请求体**:
```json
{
  "video_file_id": "video_123456",
  "audio_file_id": "audio_789012",
  "ref_image_file_id": "image_345678",
  "video_extension": true
}
```
或使用URL方式：
```json
{
  "video_url": "http://localhost:8000/api/files/videos/123456/download",
  "audio_url": "http://localhost:8000/api/files/audio/789012/download",
  "ref_image_url": "http://localhost:8000/api/files/images/345678/download",
  "video_extension": true
}
```
- **参数**:
  - `wait_completion` (bool): 是否等待任务完成，默认false
  - `request_host` (string): 请求主机，默认localhost:8000
- **文件要求**:
  - 视频：mp4、avi、mov格式，≤300MB，2-120秒，15-60fps
  - 音频：wav、mp3、aac格式，≤30MB，2-120秒
  - 参考图片：jpeg、jpg、png、bmp、webp格式，≤10MB
- **响应示例**:
```json
{
  "task_id": "uuid-video-task-id",
  "status": "PENDING",
  "message": "任务已提交，正在异步处理中"
}
```



### 6.2 获取视频任务列表
- **路径**: `GET /api/videoretalk/tasks`
- **描述**: 获取用户的视频生成任务列表
- **认证**: 需要认证
- **参数**:
  - `limit` (int): 返回数量限制，默认10
  - `offset` (int): 偏移量，默认0
- **响应示例**:
```json
{
  "tasks": [
    {
      "task_id": "uuid-video-task-id",
      "status": "SUCCEEDED",
      "message": "视频生成完成",
      "created_at": "2024-01-01T10:00:00"
    }
  ],
  "total": 5,
  "limit": 10,
  "offset": 0
}
```

### 6.3 删除视频任务
- **路径**: `DELETE /api/videoretalk/task/{task_id}`
- **描述**: 删除视频生成任务记录
- **认证**: 需要认证
- **参数**:
  - `task_id` (string): 任务ID
- **响应示例**:
```json
{
  "message": "任务 uuid-video-task-id 已删除"
}
```

### 6.4 绿幕背景替换
- **路径**: `POST /api/videoretalk/chroma-key`
- **描述**: 对视频进行绿幕背景替换处理
- **认证**: 需要认证
- **请求体**:
```json
{
  "video_file_id": "video_123456",
  "background_image_file_id": "image_789012",
  "chroma_key_color": "green",
  "chroma_key_similarity": 0.4,
  "chroma_key_blend": 0.1
}
```
- **响应示例**:
```json
{
  "task_id": "uuid-chroma-key-task-id",
  "status": "PENDING",
  "message": "绿幕背景替换任务已提交，正在异步处理中"
}
```
- **任务状态查询**: 使用统一任务状态查询接口 `GET /api/task/{task_id}` 查询处理进度

---

## 7. 文件管理 API (files.py)

### 7.1 统一文件上传
- **路径**: `POST /api/files/upload`
- **描述**: 统一文件上传接口，支持持久化存储和临时存储
- **认证**: 需要认证
- **参数**:
  - `storage_type` (string, 可选): 存储类型，默认为`persistent`
    - `persistent`: 持久化存储（需要指定file_type）
    - `temp`: 临时存储（无需file_type）
  - `file_type` (string, 可选): 文件类型，仅persistent存储时需要
    - `digital_humans`: 数字人视频
    - `backgrounds`: 背景图片  
    - `bgm`: 背景音乐
- **请求方式**: multipart/form-data

**存储类型说明**:

**persistent 存储**:
- **文件限制**:
  - digital_humans: mp4、avi、mov、mkv格式，≤500MB
  - backgrounds: jpg、jpeg、png、bmp、webp格式，≤10MB
  - bgm: mp3、wav、aac、flac格式，≤50MB

**temp 存储**:
- **文件限制**: 任意格式，≤50MB

**请求示例**:
```bash
# 上传持久化文件（数字人视频）
curl -X POST "http://localhost:8000/api/files/upload?storage_type=persistent&file_type=digital_humans" \
  -H "Authorization: Bearer <token>" \
  -F "file=@video.mp4"

# 上传临时文件
curl -X POST "http://localhost:8000/api/files/upload?storage_type=temp" \
  -H "Authorization: Bearer <token>" \
  -F "file=@temp_audio.wav"
```

**响应示例（persistent存储）**:
```json
{
  "message": "文件上传成功",
  "file_id": "digital_humans_1_video_20240101_100000.mp4",
  "file_type": "digital_humans",
  "file_size_mb": 50.0,
  "original_filename": "video.mp4",
  "url": "/api/files/download/digital_humans_1_video_20240101_100000.mp4?storage_type=persistent",
  "saved_at": "2024-01-01T10:00:00"
}
```

**响应示例（temp存储）**:
```json
{
  "message": "文件上传成功",
  "file_id": "uuid-filename.wav",
  "filename": "temp_audio.wav",
  "size": 1024000,
  "url": "/api/files/download/uuid-filename.wav?storage_type=temp"
}
```

### 7.2 统一文件下载
- **路径**: `GET /api/files/download/{file_id}`
- **描述**: 统一文件下载接口，支持所有类型文件下载
- **认证**: 🔓 **无需认证**（公开访问，支持外部服务如dashscope使用）
- **参数**:
  - `file_id` (string): 文件ID
  - `storage_type` (string, 可选): 存储类型 (`persistent`, `cache`, `temp`)
- **响应**: 返回文件内容

**支持的存储类型**:
- `persistent`: 持久化文件（数字人、背景、BGM等）
- `cache`: 缓存文件
- `temp`: 临时文件（TTS音频、音色试听等）

**自动识别**: 如果不指定 `storage_type`，系统会根据 `file_id` 自动识别文件类型

**支持的文件类型**:
- TTS音频：`tts_audio_*`
- 音色试听：`voice_preview_{voice_id}.wav`
- 持久化文件：`{file_type}_{user_id}_*`
- 通用临时文件：任意格式

**请求示例**:
```bash
# 下载TTS音频文件（无需认证）
GET /api/files/download/tts_audio_12345

# 下载音色试听文件（无需认证）
GET /api/files/download/voice_preview_alice.wav

# 下载持久化文件（无需认证）
GET /api/files/download/digital_humans_1_video_20240101?storage_type=persistent

# 下载缓存文件（无需认证）
GET /api/files/download/cache_file_id?storage_type=cache
```

**使用场景**:
- ✅ 构建公网访问URL供外部服务使用
- ✅ 提供给dashscope等AI服务访问文件
- ✅ 前端直接访问文件资源
- ⚠️ 注意：由于无需认证，文件ID应保持私密性

### 7.3 删除文件
- **路径**: `DELETE /api/files/{file_type}/{file_id}`
- **描述**: 删除指定文件
- **认证**: 需要认证
- **参数**:
  - `file_type` (string): 文件类型
  - `file_id` (string): 文件ID
- **响应示例**:
```json
{
  "message": "文件删除成功"
}
```

### 7.4 获取用户文件列表
- **路径**: `GET /api/files/user/list`
- **描述**: 获取当前用户的文件列表
- **认证**: 需要认证
- **参数**:
  - `file_type` (string): 文件类型过滤，可选
- **响应示例**:
```json
{
  "files": [
    {
      "file_id": "digital_humans_1_video_20240101_100000.mp4",
      "file_type": "digital_humans",
      "file_size": 52428800,
      "file_size_mb": 50.0,
      "original_filename": "video.mp4",
      "saved_at": "2024-01-01T10:00:00"
    }
  ],
  "total": 1
}
```

### 7.5 管理员获取所有文件
- **路径**: `GET /api/files/admin/list`
- **描述**: 管理员获取所有文件列表
- **认证**: 需要管理员认证
- **参数**:
  - `file_type` (string): 文件类型过滤，可选
  - `user_id` (int): 用户ID过滤，可选
- **响应示例**:
```json
{
  "files": [
    {
      "file_id": "digital_humans_1_video_20240101_100000.mp4",
      "file_type": "digital_humans",
      "file_size": 52428800,
      "file_size_mb": 50.0,
      "original_filename": "video.mp4",
      "user_id": 1,
      "saved_at": "2024-01-01T10:00:00"
    }
  ],
  "total": 1,
  "file_type_filter": null,
  "user_id_filter": null
}
```

### 7.6 获取文件统计信息
- **路径**: `GET /api/files/stats`
- **描述**: 获取文件统计信息（管理员）
- **认证**: 需要管理员认证
- **响应示例**:
```json
{
  "persistent_files_stats": {
    "videos": 5,
    "digital_humans": 3,
    "backgrounds": 10,
    "bgm": 7,
    "audio": 15,
    "total_files": 40,
    "total_size": 1073741824
  },
  "filesystem_stats": {
    "total_files": 100,
    "total_size": 2147483648,
    "temp_files": 20
  }
}
```

### 7.7 缓存文件管理

#### 获取缓存文件列表
- **路径**: `GET /api/files/cache/list`
- **描述**: 获取缓存文件列表
- **认证**: 无需认证
- **参数**:
  - `file_type` (string): 文件类型过滤，可选
  - `limit` (int): 返回数量限制，默认20
  - `offset` (int): 偏移量，默认0
  - `is_temp` (bool): 是否临时文件过滤，可选

#### 获取缓存文件信息
- **路径**: `GET /api/files/cache/{file_id}`
- **描述**: 获取缓存文件信息
- **认证**: 需要认证
- **参数**:
  - `file_id` (string): 文件ID

#### 删除缓存文件
- **路径**: `DELETE /api/files/cache/{file_id}`
- **描述**: 删除缓存文件
- **认证**: 需要认证
- **参数**:
  - `file_id` (string): 文件ID

---

## 8. 用户活动 API (activities.py)

### 8.1 获取最近活动记录
- **路径**: `GET /api/activities/recent`
- **描述**: 获取最近的用户活动记录
- **认证**: 需要认证
- **参数**:
  - `limit` (int): 返回记录数量，默认20，范围1-100
  - `offset` (int): 偏移量，默认0
  - `days` (int): 查询最近几天的记录，默认7，范围1-30
  - `activity_type` (string): 活动类型筛选，可选
  - `status` (string): 状态筛选，可选
- **请求示例**:
```
GET /api/activities/recent?limit=10&offset=0&days=7&activity_type=tts_generate&status=success
```
- **响应示例**:
```json
{
  "activities": [
    {
      "id": "2024-01-01T10:00:00_1",
      "timestamp": "2024-01-01T10:00:00",
      "user_id": 1,
      "user_account": "testuser",
      "activity_type": "tts_generate",
      "description": "用户 testuser 创建TTS合成任务：这是测试文本...",
      "status": "success",
      "icon": "Microphone",
      "status_color": "success",
      "formatted_time": "2小时前",
      "extra_data": {
        "task_id": "tts_123456",
        "voice": "zhichu",
        "text_length": 50
      }
    }
  ],
  "total": 1,
  "has_more": false
}
```

### 8.2 获取活动类型
- **路径**: `GET /api/activities/types`
- **描述**: 获取所有可用的活动类型
- **认证**: 需要认证
- **响应示例**:
```json
{
  "activity_types": [
    {
      "value": "user_login_success",
      "label": "登录成功",
      "icon": "User"
    },
    {
      "value": "tts_generate",
      "label": "语音合成",
      "icon": "Microphone"
    },
    {
      "value": "voice_clone",
      "label": "音色克隆",
      "icon": "CopyDocument"
    }
  ]
}
```

### 8.3 获取活动统计信息
- **路径**: `GET /api/activities/stats`
- **描述**: 获取活动统计信息（管理员权限）
- **认证**: 需要管理员认证
- **参数**:
  - `days` (int): 统计最近几天的数据，默认7，范围1-30
- **响应示例**:
```json
{
  "total_activities": 100,
  "type_stats": {
    "user_login_success": 25,
    "tts_generate": 30,
    "voice_clone": 10,
    "video_generate": 15,
    "asr_recognize": 20
  },
  "status_stats": {
    "success": 85,
    "failed": 10,
    "warning": 3,
    "info": 2
  },
  "daily_stats": {
    "2024-01-01": 20,
    "2024-01-02": 15,
    "2024-01-03": 25
  },
  "period_days": 7
}
```

---

## 9. 任务管理 API (tasks.py)

### 9.1 获取用户任务列表
- **路径**: `GET /api/tasks/`
- **描述**: 获取当前用户的任务列表
- **认证**: 需要认证
- **参数**:
  - `task_type` (string): 任务类型过滤，可选
  - `status` (string): 状态过滤，可选
  - `page` (int): 页码，默认1
  - `page_size` (int): 每页大小，默认20，范围1-100
- **请求示例**:
```
GET /api/tasks/?task_type=TTS&status=COMPLETED&page=1&page_size=10
```
- **响应示例**:
```json
{
  "tasks": [
    {
      "id": "task_123456",
      "task_type": "TTS",
      "status": "COMPLETED",
      "title": "语音合成任务",
      "description": "合成文本：这是测试内容",
      "input_data": {
        "text": "这是测试内容",
        "voice": "zhichu"
      },
      "output_data": {
        "file_id": "audio_789012",
        "file_size_mb": 2.5
      },
      "progress": 100,
      "current_step": "completed",
      "error_message": null,
      "created_at": "2024-01-01T10:00:00",
      "updated_at": "2024-01-01T10:01:30",
      "completed_at": "2024-01-01T10:01:30"
    }
  ],
  "total": 1,
  "page": 1,
  "page_size": 10
}
```

### 9.2 获取任务详情
- **路径**: `GET /api/tasks/{task_id}`
- **描述**: 获取指定任务的详细信息
- **认证**: 需要认证（只能查看自己的任务）
- **参数**:
  - `task_id` (string): 任务ID
- **响应示例**:
```json
{
  "id": "task_123456",
  "task_type": "TTS",
  "status": "COMPLETED",
  "title": "语音合成任务",
  "description": "合成文本：这是测试内容",
  "input_data": {
    "text": "这是测试内容",
    "voice": "zhichu"
  },
  "output_data": {
    "file_id": "audio_789012",
    "file_size_mb": 2.5
  },
  "progress": 100,
  "current_step": "completed",
  "error_message": null,
  "created_at": "2024-01-01T10:00:00",
  "updated_at": "2024-01-01T10:01:30",
  "completed_at": "2024-01-01T10:01:30"
}
```

### 9.3 更新任务
- **路径**: `PUT /api/tasks/{task_id}`
- **描述**: 更新任务状态和信息
- **认证**: 需要认证（只能更新自己的任务）
- **参数**:
  - `task_id` (string): 任务ID
- **请求体**:
```json
{
  "status": "FAILED",
  "error_message": "处理失败：文件格式不支持",
  "progress": 50,
  "current_step": "validation_failed"
}
```
- **响应**: 返回更新后的任务信息

### 9.4 删除任务
- **路径**: `DELETE /api/tasks/{task_id}`
- **描述**: 删除指定任务
- **认证**: 需要认证（只能删除自己的任务）
- **参数**:
  - `task_id` (string): 任务ID
- **响应示例**:
```json
{
  "message": "任务删除成功",
  "task_id": "task_123456"
}
```

### 9.5 获取任务统计信息
- **路径**: `GET /api/tasks/stats/summary`
- **描述**: 获取当前用户的任务统计信息
- **认证**: 需要认证
- **响应示例**:
```json
{
  "user_id": 1,
  "statistics": {
    "total_tasks": 50,
    "completed_tasks": 40,
    "failed_tasks": 5,
    "pending_tasks": 3,
    "running_tasks": 2,
    "task_types": {
      "TTS": 20,
      "ASR": 15,
      "VIDEO": 10,
      "VOICE_CLONE": 5
    }
  },
  "timestamp": "2024-01-01T10:00:00"
}
```

### 9.6 管理员功能

#### 获取所有任务列表
- **路径**: `GET /api/tasks/admin/all`
- **描述**: 管理员获取所有任务列表
- **认证**: 需要管理员认证
- **参数**:
  - `user_id` (int): 用户ID过滤，可选
  - `task_type` (string): 任务类型过滤，可选
  - `status` (string): 状态过滤，可选
  - `page` (int): 页码，默认1
  - `page_size` (int): 每页大小，默认20

#### 获取全局任务统计
- **路径**: `GET /api/tasks/admin/stats/global`
- **描述**: 获取全局任务统计信息
- **认证**: 需要管理员认证
- **响应示例**:
```json
{
  "global_statistics": {
    "total_tasks": 1000,
    "completed_tasks": 800,
    "failed_tasks": 100,
    "pending_tasks": 50,
    "running_tasks": 50,
    "task_types": {
      "TTS": 400,
      "ASR": 300,
      "VIDEO": 200,
      "VOICE_CLONE": 100
    },
    "user_distribution": {
      "total_users": 50,
      "active_users": 30
    }
  },
  "timestamp": "2024-01-01T10:00:00"
}
```

---

## 10. 系统监控 API (health.py)

### 10.1 统一系统状态接口
- **路径**: `GET /api/system`
- **描述**: 获取完整的系统状态信息，整合了原有的健康检查、服务状态、缓存配置等功能
- **认证**: 无需认证
- **参数**:
  - `include_cache` (bool): 是否包含缓存配置信息，默认false
  - `include_resources` (bool): 是否包含系统资源使用情况，默认false
- **请求示例**:
```
# 基础系统状态
GET /api/system

# 包含系统资源使用情况
GET /api/system?include_resources=true

# 包含缓存配置信息
GET /api/system?include_cache=true

# 获取最完整的系统状态
GET /api/system?include_resources=true&include_cache=true
```
- **响应示例**（完整版本）:
```json
{
  "name": "AI视频生成服务平台",
  "version": "1.0.0",
  "description": "提供语音识别、语音合成、视频生成等AI服务",
  "status": "running",
  "timestamp": "2024-01-01T10:00:00",
  "overall_status": "healthy",
  "uptime": {
    "seconds": 9045,
    "human_readable": "2:30:45",
    "started_at": "2024-01-01T07:29:15"
  },
  "features": [
    "语音识别 (ASR)",
    "语音合成 (TTS)",
    "视频生成 (VideoRetalk)",
    "绿幕背景替换",
    "语音克隆",
    "用户管理",
    "任务管理"
  ],
  "endpoints": {
    "user_management": "/api/user",
    "asr": "/api/asr",
    "tts": "/api/tts",
    "llm": "/api/llm",
    "video": "/api/videoretalk",
    "tasks": "/api/tasks",
    "files": "/api/files",
    "activities": "/api/activities",
    "system": "/api/system"
  },
  "services": {
    "asr": {
      "status": "running",
      "name": "语音识别服务"
    },
    "llm": {
      "status": "running", 
      "name": "大语言模型服务"
    },
    "tts": {
      "status": "running",
      "name": "语音合成服务"
    },
    "video": {
      "status": "running",
      "name": "视频生成服务"
    },
    "database": {
      "status": "connected",
      "name": "数据库"
    },
    "storage": {
      "status": "available",
      "name": "文件存储"
    }
  },
  "system_resources": {
    "cpu_usage": "15.2%",
    "memory_usage": "45.8%",
    "available_memory": "2.75GB",
    "total_memory": "5.00GB",
    "disk_usage": "60.3%",
    "available_disk": "150.25GB",
    "total_disk": "500.00GB"
  },
  "cache_config": {
    "global_temp_config": {
      "temp_dir": "/tmp",
      "exists": true,
      "writable": true
    },
    "services_config": {
      "tts": {
        "temp_dir": "/tmp",
        "uses_config_temp_dir": true,
        "status": "initialized"
      }
    },
    "validation": {
      "temp_dir_valid": true,
      "all_services_use_config": true
    }
  },
  "documentation": "/docs",
  "api_version": "v1"
}
```
