Universal Decompiler

A universal, automated decompilation workflow powered entirely by GitHub Actions.

Upload supported files to the repository, commit your changes, and GitHub Actions automatically detects and decompiles them. No local installations or dependencies required.

Supported formats

File type| Processing
APK| JADX + Apktool
DEX| JADX
JAR| JADX
CLASS| JADX
AAR| JADX
AAB| JADX
ZIP| JADX
XAPK| JADX
APKM| JADX
APKS| JADX

JADX extracts Java source code, while Apktool decodes Android resources and Smali code from APKs.

How to use

1. Upload your files anywhere in the repository.
2. Commit and push your changes to "main".
3. Open the Actions tab.
4. Wait for the decompilation workflow to finish.
5. Download the "decompiled-files" artifact.

That's it!

Results

All decompiled files are packaged into a single downloadable ZIP artifact.

The original repository remains untouched by the decompilation process. Generated files are stored temporarily on the GitHub Actions runner.

Artifacts are retained for 7 days.

Technologies

- "GitHub Actions" (https://github.com/features/actions)
- "JADX" (https://github.com/skylot/jadx)
- "Apktool" (https://github.com/iBotPeaches/Apktool)

Notes

- Previously uploaded supported files are processed again on subsequent pushes.
- Unsupported file types are skipped.
- Individual decompilation failures do not necessarily stop the entire workflow.
- Large files may take longer to process.
- This project is intended for legitimate software inspection and reverse engineering.

License

See the repository's license file.
