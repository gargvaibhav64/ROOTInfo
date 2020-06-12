# ROOTInfo

Use the following to launch debugger on RootCling on Windows:

```
devenv /debugexe E:/root-build/bin/rootcling_stage1.exe -v2 -f G__Core.cxx -cxxmodule -s E:/root-build/bin/libCore.dll -excludePath E:/root -excludePath E:/root-build/ginclude -excludePath E:/root-build/externals -excludePath E:/root-build/builtins -IE:/root-build/include -IE:/root-build/ginclude -IE:/root/core/base/inc -IE:/root/core/foundation/inc -IE:/root/core/cont/inc -IE:/root/core/gui/inc -IE:/root/core/meta/inc -IE:/root/core/clib/inc -IE:/root/core/rint/inc -IE:/root/core/zip/inc -IE:/root/core/thread/inc -IE:/root/core/textinput/inc -IE:/root/core/clingutils/inc -IE:/root/core/base/v7/inc -IE:/root/core/winnt/inc -IE:/root-build/builtins/pcre/PCRE-prefix/src/PCRE-build -IE:/root/builtins/xxhash -IE:/root/builtins/lz4 -IE:/root/builtins/zlib -IE:/root/builtins/zstd -writeEmptyRootPCM ROOT/StringConv.hxx ROOT/TExecutor.hxx ROOT/TSequentialExecutor.hxx Buttons.h Bytes.h Byteswap.h KeySymbols.h MessageTypes.h Riostream.h Rtypes.h TApplication.h TAtt3D.h TAttAxis.h TAttBBox2D.h TAttBBox.h TAttFill.h TAttLine.h TAttMarker.h TAttPad.h TAttText.h TBase64.h TBenchmark.h TBuffer3D.h TBuffer3DTypes.h TBuffer.h TColor.h TColorGradient.h TDatime.h TDirectory.h TEnv.h TError.h TException.h TExec.h TFileCollection.h TFileInfo.h TFolder.h TInetAddress.h TMacro.h TMathBase.h TMD5.h TMemberInspector.h TMessageHandler.h TNamed.h TNotifyLink.h TObject.h TObjString.h TParameter.h TPluginManager.h TPoint.h TPRegexp.h TProcessID.h TProcessUUID.h TQClass.h TQCommand.h TQConnection.h TQObject.h TRedirectOutputGuard.h TRefCnt.h TRef.h TRegexp.h TRemoteObject.h TROOT.h TRootIOCtor.h TStopwatch.h TStorage.h TString.h TStringLong.h TStyle.h TSysEvtHandler.h TSystemDirectory.h TSystemFile.h TSystem.h TTask.h TThreadSlots.h TTime.h TTimer.h TTimeStamp.h TUri.h TUrl.h TUUID.h TVersionCheck.h TVirtualAuth.h TVirtualFFT.h TVirtualGL.h TVirtualMonitoring.h TVirtualMutex.h TVirtualPadEditor.h TVirtualPad.h TVirtualPadPainter.h TVirtualPerfStats.h TVirtualPS.h TVirtualQConnection.h TVirtualRWMutex.h TVirtualTableInterface.h TVirtualViewer3D.h TVirtualX.h ROOT/RLogger.hxx ROOT/RDirectoryEntry.hxx ROOT/RError.hxx ROOT/RIndexIter.hxx strlcpy.h snprintf.h ROOT/TSeq.hxx TArrayC.h TArrayD.h TArrayF.h TArray.h TArrayI.h TArrayL64.h TArrayL.h TArrayS.h TBits.h TBtree.h TClassTable.h TClonesArray.h TCollection.h TCollectionProxyInfo.h TExMap.h THashList.h THashTable.h TIterator.h TList.h TMap.h TObjArray.h TObjectTable.h TOrdCollection.h TRefArray.h TRefTable.h TSeqCollection.h TSortedList.h TVirtualCollectionProxy.h ESTLType.h RStringView.h TClassEdit.h ROOT/RIntegerSequence.hxx ROOT/RMakeUnique.hxx ROOT/RNotFn.hxx ROOT/RSpan.hxx ROOT/RStringView.hxx ROOT/span.hxx ROOT/TypeTraits.hxx TWinNTSystem.h root_std_complex.h GuiTypes.h TApplicationImp.h TBrowser.h TBrowserImp.h TCanvasImp.h TClassMenuItem.h TContextMenu.h TContextMenuImp.h TControlBarImp.h TGuiFactory.h TInspectorImp.h TObjectSpy.h TToggleGroup.h TToggle.h TBaseClass.h TClassGenerator.h TClass.h TClassRef.h TClassStreamer.h TDataMember.h TDataType.h TDictAttributeMap.h TDictionary.h TEnumConstant.h TEnum.h TFileMergeInfo.h TFunction.h TFunctionTemplate.h TGenericClassInfo.h TGlobal.h TInterpreter.h TInterpreterValue.h TIsAProxy.h TListOfDataMembers.h TListOfEnums.h TListOfEnumsWithLock.h TListOfFunctions.h TListOfFunctionTemplates.h TMemberStreamer.h TMethodArg.h TMethodCall.h TMethod.h TProtoClass.h TRealData.h TSchemaHelper.h TSchemaRule.h TSchemaRuleSet.h TStatusBitsChecker.h TStreamerElement.h TStreamer.h TVirtualIsAProxy.h TVirtualRefProxy.h TVirtualStreamerInfo.h TVirtualArray.h TVirtualObject.h Getline.h E:/root/core/base/inc/LinkDef.h
```

For configuring CMake on Windows

Debug
```
cmake -G "Visual Studio 16 2019" -A Win32 -Thost=x64 -DCMAKE_VERBOSE_MAKEFILE=ON -DCMAKE_CXX_STANDARD=14 -Dtesting=Off -Druntime_cxxmodules=On -DLLVM_BUILD_TYPE=Debug -Dpyroot=Off ../root
```
Release
```
cmake -G "Visual Studio 16 2019" -A Win32 -Thost=x64 -DCMAKE_VERBOSE_MAKEFILE=ON -DCMAKE_CXX_STANDARD=14 -Dtesting=Off -Druntime_cxxmodules=On -Dpyroot=Off ../root
```

For building using CMake on Windows
```
cmake --build . --config [Debug|Release]
```
For Single CPU
```
cmake --build . --config Debug -- /maxcpucount:1
```
For Building a Upto Target X
```
cmake --build . --target X --config Debug -- /maxcpucount:1
```




