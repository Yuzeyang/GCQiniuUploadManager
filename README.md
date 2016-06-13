# GCQiniuUploadManager

## Introduction

It provide simple interfaces to create token,upload file and upload files

## how to use

1.register with your scope, access key and secret key and create token in your AppDelegate.m

```objective-c
[[CJQiniuUploadManager sharedInstance] registerWithScope:CJQiNiuScope
                                                   accessKey:CJQiNiuAccessKey
                                                   secretKey:CJQiNiuSecretKey];
[[CJQiniuUploadManager sharedInstance] createToken];
```

2.you can upload single data

```objective-c
- (void)uploadData:(NSData *)data
          progress:(UploadProgressHandler)progress
        completion:(UploadDataCompletion)completion;
```

3.you can also upload multiple data

```objective-c
- (void)uploadDatas:(NSArray<NSData *> *)datas
           progress:(UploadProgressHandler)progress
  oneTaskCompletion:(UploadDataCompletion)oneTaskCompletion
 allTasksCompletion:(UploadAllTasksCompletion)allTasksCompletion;
```

4.you can set upload token live time，it default is 5 days

```objective-c
@property (nonatomic, assign) NSInteger liveTime;
```

