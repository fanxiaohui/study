``` 
typedef struct 
{
	INT16U  Function;
	int     (*MsgExeFun)(CAN_MSG_DATA * pMsg, INT8U *pData);
	
}CAN_MSG_CMD;

const CAN_MSG_CMD CmdList[] =
{
	{WCHAR('1', 'E'), MsgRdVerFun},					// 读取版本号

	{WCHAR('0', 'I'), MsgRdSysTimeFun},				// 读系统时间
	{WCHAR('1', 'I'), MsgWrSysTimeFun},				// 写系统时间
}


//调用
	result = pMsgCmd->MsgExeFun(pMsg, (INT8U *)0);



``` 
