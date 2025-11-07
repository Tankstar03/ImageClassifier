**Model Metrics**



**Model A: ResNet-50**

**Model Head** 

	x = Flatten()(base_model.output)
	x = Dense(256, activation='relu')(x)
	x = Dropout(0.5)(x)
	output = Dense(1, activation='sigmoid')(x)

**Model Layers (excluding Head)	|	Layer Count**

	InputLayer			|	1
	Conv2D				|	53
	BatchNormalization	|	53
	Activation			|	49
	Add					|	16
	ZeroPadding2D		|	2
	Dense				|	2
	MaxPooling2D		|	1
	Flatten				|	1
	Dropout				|	1

**Total layers: 179**

**Performance Metrics**

| Training Accuracy | Training Loss | Validation Accuracy | Validation Loss | Training Time (seconds) |
| ----------------- | ------------- | ------------------- | --------------- | ----------------------- |
| 0.81122 | 3.39254 | 0.87473 | 0.28523 | 519 |
| 0.90063 | 0.25507 | 0.89356 | 0.29990	| 334 |
| 0.92670 | 0.18457 | 0.88849 | 0.27270	| 329 |
| 0.94226 | 0.14228 | 0.90152 | 0.35298	| 400 | 
| 0.94443 | 0.13904 | 0.89718 | 0.36680	| 324 |
| 0.95149 | 0.12563 | 0.92035 | 0.25958	| 413 |
| 0.96235 | 0.10722 | 0.91745 | 0.29011	| 360 |
| 0.96452 | 0.10224	| 0.91890 | 0.26554	| 333 |
| 0.97285 | 0.07054	| 0.92542 | 0.31961	| 324 |
| 0.96977 | 0.07654	| 0.90587 | 0.35572	| 326 |

**Testing accuracy and loss: [0.9090, 0.3518]**		



**Model B: ConvNeXtBase**

**Model Head**

	x = GlobalAveragePooling2D()(base_model.output)
	x = Dropout(0.5)(x)
	x = Dense(256, activation='relu')(x)
	x = Dropout(0.3)(x)		
	output = Dense(1, activation='sigmoid')(x)

**Model Layers (excluding Head)	|	Layer Count**

	InputLayer				|	1
	Dense					|	74
	Activation				|	72
	LayerNormalization		|	37
	LayerScale				|	36
	Conv2D					|	36
	Add						|	36
	Sequential				|	4
	Dropout					|	2
	Normalization			|	1
	GlobalAveragePooling2D	|	1

**Total Layers: 300**

**Performance Metrics**

| Training Accuracy | Training Loss	| Validation Accuracy | Validation Loss	| Training Time (seconds) |
| ----------------- | ------------- | ------------------- | --------------- | ----------------------- |
| 0.87167 | 0.28760	| 0.92035 | 0.19772	| 5309 |
| 0.91729 | 0.20856	| 0.92542 | 0.17861	| 4862 |
| 0.92525 | 0.17895	| 0.93049 | 0.17323 | 5848 |
| 0.93557 | 0.16055	| 0.92324 | 0.18479	| 4748 |
| 0.93882 | 0.14998	| 0.93049 | 0.16255	| 4784 |
| 0.94425 | 0.14042	| 0.92759 | 0.17633	| 4848 |
| 0.95204 | 0.11977	| 0.92686 | 0.18016	| 4855 |
| 0.95674 | 0.11545	| 0.93700 | 0.16700	| 4872 |
| 0.95855 | 0.10541	| 0.93121 | 0.16941	| 4635 |
| 0.96181 | 0.09932	| 0.92759 | 0.18003	| 2802 |

**Testing accuracy and loss: [0.9404, 0.1569]**