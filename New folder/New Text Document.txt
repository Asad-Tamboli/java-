
def _find_misplaced_java_files() -> list[pathlib.Path]:
    return [
        java_file
        for java_file in pathlib.Path(".").rglob("*.java")
        if not _is_java_file_properly_located(java_file)
    ]

