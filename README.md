qa_hw_10
Windows PowerShell
(C) Корпорация Майкрософт (Microsoft Corporation). Все права защищены.

Попробуйте новую кроссплатформенную оболочку PowerShell (https://aka.ms/pscore6)

PS C:\Users\USER> cd C:\
PS C:\> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser

Изменение политики выполнения
Политика выполнения защищает компьютер от ненадежных сценариев. Изменение политики выполнения может поставить под
угрозу безопасность системы, как описано в разделе справки, вызываемом командой about_Execution_Policies и
расположенном по адресу https:/go.microsoft.com/fwlink/?LinkID=135170 . Вы хотите изменить политику выполнения?
[Y] Да - Y  [A] Да для всех - A  [N] Нет - N  [L] Нет для всех - L  [S] Приостановить - S  [?] Справка
(значением по умолчанию является "N"):Y
PS C:\> Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression
Initializing...
Downloading...
Creating shim...
Adding ~\scoop\shims to your path.
Scoop was installed successfully!
Type 'scoop help' for instructions.
PS C:\> scoop install allure
Installing 'allure' (2.29.0) [64bit] from 'main' bucket
allure-2.29.0.zip (35,5 MB) [=================================================================================] 100%
Checking hash of allure-2.29.0.zip ... ok.
Extracting allure-2.29.0.zip ... done.
Linking ~\scoop\apps\allure\current => ~\scoop\apps\allure\2.29.0
Creating shim for 'allure'.
'allure' (2.29.0) was installed successfully!
PS C:\> C:\Users\USER\scoop\apps\allure\2.29.0\bin\allure.bat
Usage: allure [options] [command] [command options]
  Options:
    --help
      Print commandline help.
    -q, --quiet
      Switch on the quiet mode.
      Default: false
    -v, --verbose
      Switch on the verbose mode.
      Default: false
    --version
      Print commandline version.
      Default: false
  Commands:
    generate      Generate the report
      Usage: generate [options] The directories with allure results
        Options:
          -c, --clean
            Clean Allure report directory before generating a new one.
            Default: false
          --config
            Allure commandline config path. If specified overrides values from
            --profile and --configDirectory.
          --configDirectory
            Allure commandline configurations directory. By default uses
            ALLURE_HOME directory.
          --profile
            Allure commandline configuration profile.
          -o, --report-dir, --output
            The directory to generate Allure report into.
            Default: allure-report
          --lang, --report-language
            The report language.
          --name, --report-name
            The report name.
          --single-file
            Generate Allure report in single file mode.
            Default: false

    serve      Serve the report
      Usage: serve [options] The directories with allure results
        Options:
          --config
            Allure commandline config path. If specified overrides values from
            --profile and --configDirectory.
          --configDirectory
            Allure commandline configurations directory. By default uses
            ALLURE_HOME directory.
          -h, --host
            This host will be used to start web server for the report.
          -p, --port
            This port will be used to start web server for the report.
            Default: 0
          --profile
            Allure commandline configuration profile.
          --lang, --report-language
            The report language.
          --name, --report-name
            The report name.

    open      Open generated report
      Usage: open [options] The report directory
        Options:
          -h, --host
            This host will be used to start web server for the report.
          -p, --port
            This port will be used to start web server for the report.
            Default: 0

    plugin      Display plugins
      Usage: plugin [options]
        Options:
          --config
            Allure commandline config path. If specified overrides values from
            --profile and --configDirectory.
          --configDirectory
            Allure commandline configurations directory. By default uses
            ALLURE_HOME directory.
          --profile
            Allure commandline configuration profile.


PS C:\> C:\Users\USER\scoop\apps\allure\2.29.0\bin\allure.bat serve
Generating report to temp directory...
allure-results does not exist
Report successfully generated to C:\Users\0982~1\AppData\Local\Temp\6798206390111832397\allure-report
Starting web server...
2024-05-16 00:20:02.489:INFO::main: Logging initialized @2739ms to org.eclipse.jetty.util.log.StdErrLog
Server started at <http://192.168.152.153:51421/>. Press <Ctrl+C> to exit
