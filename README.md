这是接入广州社保的DLL，由于还在使用，不提供源码，只提供使用办法和DLL编译后的程序在Release


	 int  postgzsbinv(const char * accessKey, const char * secreKey, 
		const char * rtalPhacCodg,const char * rtalPhacName, const char * buymedDocCodg, 
		const double selAmtotal,const char * buymedDate, const char * authPhacCodg, const char * tranIdSn,
		const char * crterName, int recordscount, const char ** medinsListCodg, double * rtalPric,
		double * selCnt, double * selAmt, const char ** manuLotnum, 
		int returncode, char * retype, char * retmsg);


	 int  postgzsbprodep(const char * accessKey, const char * secreKey,
		const char * authPhacCodg, const char * rtalPhacCodg, const char * rtalPhacName,
		const char * admdvs, const char * fixmedinsBchno, int recordscount,
		const char ** medListCodg, const char ** medListName, const char ** medinsListCodg,
		const char ** medinsListName, const char ** rxFlag, double * invCnt, const char ** manuLotnum,
		const char ** manuDate, const char ** expyEnd, const char ** invDate, const char** memo,
		const char ** spec, const char ** dosformType, 
		int returncode, char * retype, char * retmsg);

	int postgzsbdepretinvback(const char * accessKey, const char * secreKey,
		const char * authPhacCodg, const char * rtalPhacCodg,
		const char * rtalPhacName, const char * admdvs, const char * fixmedinsBchno,
		const char * supnDocType, int recordscount, const char ** selDocSn,
		const char ** dyntNo, const char** splerName, const char ** purcInvoNo,
		const char ** memo, const char ** medListCodg, const char ** medListName,
		const char ** medinsListCodg, const char ** medinsListName, const char ** manuLotnum,
		const char ** manuDate, const char ** expyEnd, const char** prodentpName, const char ** aprvno,
		const char ** spec, const char ** dosformType, double * finlTrnsPric, const char ** rxFlag,
		const char ** certno, const char ** psnCertType, const char ** psnName, double * purcRetnCnt,
		const char ** purcRetnStoinTime, const char ** purcRetnOpterName, double * selRetnCnt,
		const char ** selRetnTime, const char ** selRetnOpterName, const char ** setlId,
		const char ** prscDrCertType, const char ** prscDrCertno, const char ** bilgdrName,
		const char ** pharCertType, const char ** pharcertno, const char ** pharName,
		const char ** pharpracCertNo, const char ** hiFeesetlType, const char ** psnNo,
		const char ** trdnFlag, const char ** mdtrtSn,
		int returncode, char * retype, char * retmsg);

	int postgzsbprodepalter(const char * accessKey, const char * secreKey,
		const char * authPhacCodg, const char * rtalPhacCodg,
		const char * rtalPhacName, const char * admdvs, const char * fixmedinsBchno,
		int recordscount, const char ** medListCodg, const char ** medListName,
		const char ** invChgType, const char ** medinsListCodg, const char ** medinsListName,
		double * pric, double * cnt, const char ** rxFlag, const char ** invChgTime,
		const char ** invChgOpterName, const char ** memo, 
		int returncode, char * retype, char * retmsg);

	int  postgzsbdelprodep(const char * accessKey, const char * secreKey,
		const char * authPhacCodg, const char * rtalPhacCodg,
		const char * fixmedinsBchno, const char * invDataType, 
		int returncode, char * retype, char * retmsg);


	int  postgzsbaddprod(const char * accessKey, const char * secreKey,
		const char * authPhacCodg, const char * rtalPhacCodg, const char * listType, const char * dosformType,
		const char * drugadmStrdcod, const char * spec, const char * medinsListCodg,
		const char * medinsListName, const char * prdr, const char * aprvno,
		const char * prodplac, const char * drugProdname, const char * rxFlag,
		const char * prodMol, const char * specMol, const char * medEquMgtType,
		const char * regFilNo, char * retmedinsListInfoSn, char * retmedinsListCodg,
		char * retpinyin, char *retwubi,  int returncode,
		char * retype, char * retmsg);


	 int  postgzsbalterprod(const char * accessKey, const char * secreKey,
		const char * medinsListInfoSn, const char * medinsListCodg, const char * authPhacCodg, const char * rtalPhacCodg,
		const char * listType, const char * dosformType, const char * drugadmStrdcod,
		const char * spec, const char * medinsListName, const char * prdr, const char * aprvno,
		const char * prodplac, const char * drugProdname, const char * rxFlag,
		const char * prodMol, const char * specMol, const char * medEquMgtType,
		const char * regFilNo, char * retmedinsListInfoSn, char * retmedinsListCodg,
		char * retpinyin, char * retwubi, char * retrtalPhacCodg, char * retlistType,
		char * retdosformType, char * retdrugadmStrdcod, char * retspec,
		char * retmedinsListName, char * retprdr, char * retaprvno, char * retprodplac,
		char * retdrugProdname, char * retrxFlag, char * retprodMol, char * retspecMol,
		char * retmedEquMgtType, char * retregFilNo,  int returncode,
		char * retype, char * retmsg);

	 int  postgzsbdelprod(const char * accessKey, const char * secreKey, const char * medinsListCodg,
		const char* medinsListInfoSn, const char * authPhacCodg, const char * rtalPhacCodg,
		int returncode, char * retype, char * retmsg);

	int querytransaction(const char * accessKey, const char * secreKey,
		const char* authPhacCodg, const char * rtalPhacCodg, const char * buymedDocCodg,
		const char * buymedDate, double & retselAmt, double & rethiAmt,
		double & retcashAmt, char * retsetlTime, char * retpurcStas,
		 int returncode, char * retype, char * retmsg);


	int queryprodrelationship(const char * accessKey, const char * secreKey,
		const char * authPhacCodg, const char * rtalPhacCodg, int pageNum,
		int pageSize, int & retpagenum, int & retpagesize, int & retsize,
		int & retstartrow, int & retendrow, int & retpages, int & rettotalrecordscount,
		int & retprepage, int & retnextpage, bool & retfirstpage, bool & retlastpage,
		int retrecordscount, char ** retrtalPhacCodg, char ** retrtalPhacName,
		char ** retmedinsListType, char ** retmedinsListCodg, char ** retmedinsListName,
		char ** retmedListCodg, char ** retmedListName, char ** retlistType,
		char ** retlistTypeName,  int returncode,
		char * retype, char * retmsg);
