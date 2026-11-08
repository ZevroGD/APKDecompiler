Universal Decompiler

A universal, automated decompilation workflow powered entirely by GitHub Actions.

Upload supported files to the repository, commit your changes, and GitHub Actions automatically detects and decompiles them. No local installations or dependencies required.

Supported formats

- APK: JADX + Apktool
- DEX: JADX
- JAR: JADX
- CLASS: JADX
- AAR: JADX
- AAB: JADX
- ZIP: JADX
- XAPK: JADX
- APKM: JADX
- APKS: JADX

JADX extracts Java source code, while Apktool decodes Android resources and Smali code from APKs.

How to use

1. Upload your files anywhere in the repository.
2. Commit and push your changes to "main".
3. GitHub Actions automatically starts the workflow.
4. Wait for decompilation to finish.
5. Download either the ZIP or TAR artifact from the Actions run.

That's it!

Results

Two downloadable artifacts are generated:

- decompiled-files-zip: Compressed ZIP archive, suitable for smaller downloads.
- decompiled-files-tar: Uncompressed TAR archive, suitable for faster extraction.

Both contain the same decompiled files.

Before uploading, both archives are checked for integrity.

Successfully processed original files are automatically deleted from the repository and the deletion is committed by GitHub Actions. Files that fail processing are kept.

Generated files are stored temporarily on the GitHub Actions runner.

Artifacts are retained for 7 days.

Technologies

- "GitHub Actions" (https://github.com/features/actions)
- "JADX" (https://github.com/skylot/jadx)
- "Apktool" (https://github.com/iBotPeaches/Apktool)

Notes

- Previously uploaded supported files are processed again on subsequent pushes if they remain in the repository.
- Successfully processed files are automatically removed.
- Unsupported file types are skipped.
- Individual decompilation failures do not necessarily stop the entire workflow.
- Failed files remain in the repository.
- Large files may take longer to process.
- The workflow requires repository write permissions to delete and commit processed files.
- This project is intended for legitimate software inspection and reverse engineering.

License

See the repository's license file.
