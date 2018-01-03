maven_jar(
    name = "asciidoctor",
    artifact = "org.asciidoctor:asciidoctorj:1.5.6",
    sha1 = "bb757d4b8b0f8438ce2ed781f6688cc6c01d9237",
)

maven_jar(
    name = "jruby",
    artifact = "org.jruby:jruby-complete:9.1.13.0",
    sha1 = "8903bf42272062e87a7cbc1d98919e0729a9939f",
)

maven_jar(
    name = "args4j",
    artifact = "args4j:args4j:2.0.26",
    sha1 = "01ebb18ebb3b379a74207d5af4ea7c8338ebd78b",
)

load("//lib:guava.bzl", "GUAVA_VERSION", "GUAVA_BIN_SHA1")

maven_jar(
    name = "guava",
    artifact = "com.google.guava:guava:" + GUAVA_VERSION,
    sha1 = GUAVA_BIN_SHA1,
)

maven_jar(
    name = "j2objc",
    artifact = "com.google.j2objc:j2objc-annotations:1.1",
    sha1 = "ed28ded51a8b1c6b112568def5f4b455e6809019",
)

SLF4J_VERS = "1.7.7"

maven_jar(
    name = "log_api",
    artifact = "org.slf4j:slf4j-api:" + SLF4J_VERS,
    sha1 = "2b8019b6249bb05d81d3a3094e468753e2b21311",
)

maven_jar(
    name = "log_nop",
    artifact = "org.slf4j:slf4j-nop:" + SLF4J_VERS,
    sha1 = "6cca9a3b999ff28b7a35ca762b3197cd7e4c2ad1",
)
